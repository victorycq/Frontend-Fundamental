<template>
  <div id="login">
    <div class="login__container">
      <div class="login__content">
        <h1>This is place for your content.</h1>
      </div>
      <div class="login__form">
        <div class="login__logo"></div>
        <div class="login__header">
          <h1>Login</h1>
          <p>See your growth and get consulting support!</p>
        </div>
        <div class="login__button">
          <button>Sign in with Google</button>
        </div>
        <div class="separator">or Sign in with Email</div>
        <form>
          <div class="field">
            <input type="text" name="name" placeholder=" " required />
            <label for="name">Enter name</label>
            <!-- <span id="error">Name is required</span> -->
          </div>
          <div class="field">
            <input
              type="password"
              name="password"
              placeholder=" "
              aria-describedby="passwordhint"
              required
            />
            <!-- <p class="field-hint" id="passwordhint">
              Must contain 8+ characters with at least 1 number and 1 uppercase
              letter.
            </p> -->
            <label for="password">Enter Password</label>
            <!-- <span id="error">Name is required</span> -->
          </div>
          <div class="login__option">
            <div class="login__remember">
              <input type="checkbox" name="remember" id="remember" />
              <label for="remember">Remember Me</label>
            </div>
            <a href="https://www.google.com/" class="login__forgetPassword">
              Forget Password?
            </a>
          </div>
          <div class="login__button">
            <input type="submit" value="Login" />
          </div>
          <div class="login__redirect">
            Not registered?
            <a href="http://google.com">Create an Account</a>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
