<script lang="ts" setup></script>
<template>
  <div class="bg"></div>
  <div class="signin-wrapper">
    <div class="signin-container">
      <div class="title-container">
        <h1 class="machina">Sign Up</h1>
      </div>
      <div class="signup-form">
        <div class="auth-signup">
          <FormInput label="email address" data-model="email" type="email" />
          <FormInput label="full name" data-model="name" />
          <FormInput label="password" data-model="password" />
          <FormInput label="confirm password" data-model="confirmpassword" />
          <UiButton class="fill"> Continue </UiButton>
        </div>

        <div class="signin-link inconsolata">
          <p>
            Already Have an account?
            <NuxtLink :to="{ path: '/signin' }">Sign in</NuxtLink>
          </p>
        </div>
      </div>

      <div class="law">
        <p class="satoshi">
          By Creating an account, you agree to our <a>Terms of Service</a> &
          <a>Privacy policy</a>
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bg {
  width: 100vw;
  height: 100vh;
  position: absolute;
  top: 0;
  left: 0;
  background-image: url(../assets/images/bg.jpg);
  z-index: -999;
  background-position: 50%;
  background-size: cover;
}

.signin-wrapper {
  width: 100%;
  padding: 24px;
  margin-top: 72px;
  position: relative;
  max-width: 1440px;
  display: flex;
  justify-content: flex-end;

  .signin-container {
    max-width: 420px;
    padding: 0px 48px;
    border: 1px solid black;
    border-radius: 16px;
    background-color: var(--color-bg);

    .title-container {
      margin-top: 48px;
    }

    .signup-form {
      margin: 36px 0;

      .auth-signup {
        button {
          margin-top: 6px;
        }
      }

      .signin-link {
        width: 100%;
        margin-top: 20px;
        text-align: center;
        font-size: 14px;

        p {
          color: var(--color-text);
          a {
            color: var(--color-text);

            &:hover {
              color: var(--color-accent);
              transition: 0.2s ease;
            }
          }
        }
      }
    }
    .law {
      padding: 24px 0;
      p {
        text-align: center;
        color: var(--color-text);
        font-size: 11px;

        a {
          color: var(--color-text);
          text-decoration: underline;
        }
      }
    }
  }
}
</style>
