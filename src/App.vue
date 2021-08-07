<template>
  <div class="container-center">
    <div class="card">
      <div>
        <input
          @change="toggleTheme"
          id="checkbox"
          type="checkbox"
          class="switch-checkbox"
        />
        <label for="checkbox" class="switch-label">
          <span>🌙</span>
          <span>☀️</span>
          <div
            class="switch-toggle"
            :class="{ 'switch-toggle-checked': theme === 'dark' }"
          ></div>
        </label>
      </div>
      <p>How to create toogle Light/Dark Mode?</p>
      <p>This is example toogle mode,</p>
      <p>It's fundamental for you.</p>
    </div>
  </div>
  <router-view></router-view>
</template>

<script>
export default {
  name: "App",
  components: {},
  mounted() {
    const initUserTheme = this.getMediaPreference();
    this.setTheme(initUserTheme);
  },

  data() {
    return {
      theme: "light",
    };
  },

  methods: {
    toggleTheme() {
      const activeTheme = localStorage.getItem("theme");
      if (activeTheme === "light") {
        this.setTheme("dark");
      } else {
        this.setTheme("light");
      }
    },

    setTheme(theme) {
      localStorage.setItem("theme", theme);
      this.theme = theme;

      let htmlElement = document.documentElement;
      htmlElement.setAttribute("theme", theme);
    },

    getMediaPreference() {
      const hasDarkPreference = window.matchMedia(
        "(prefers-color-scheme: dark)"
      ).matches;
      if (hasDarkPreference) {
        return "dark";
      } else {
        return "light";
      }
    },
  },
};
</script>
