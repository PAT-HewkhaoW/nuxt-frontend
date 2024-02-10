<script lang="ts" setup>
definePageMeta({
  layout: "default",
});
const data = reactive({
  emial: "",
  passowrd: "",
});

async function handleSigninSubmit() {}
</script>

<template>
  <!-- <div>this is sign in page</div> -->
  <div class="bg"></div>
  <div class="icon-container">
    <icons fill-color="white" iconHeight="48" />
  </div>
  <div class="signin-wrapper">
    <div class="signin-container">
      <div class="title-container">
        <h1 class="machina inktrap">Welcome Back</h1>
        <p class="inconsolata">Signin Your Account!</p>
      </div>

      <div class="signin-form">
        <div class="auth-signin">
          <formInput label="email" data-model="email" />
          <formInput label="password" data-model="password" />
          <uiButton class="fill"> continue </uiButton>
        </div>

        <div class="signup-link inconsolata">
          <p>
            No account? <NuxtLink :to="{ path: '/signup' }">Sign up</NuxtLink>
          </p>
        </div>
      </div>

      <div class="law">
        <p class="satoshi">
          By logging in, you agree to our <a>Terms of Service</a> &
          <a>Privacy policy</a>
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/base.scss";

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

.icon-container {
  padding: 32px 0;
}
.signin-wrapper {
  width: 100%;
  padding: 24px;
  margin-top: 72px;
  max-width: 1440px;
  position: relative;
  display: flex;
  justify-content: flex-end;

  @include for-mobile {
    display: grid;
    place-items: center;
  }

  .signin-container {
    max-width: 420px;
    padding: 0px 48px;
    border: 1px solid black;
    border-radius: 16px;
    background-color: var(--color-bg);

    .title-container {
      margin-top: 48px;
    }
    .signin-form {
      margin: 36px 0;

      .auth-signin {
        button {
          margin-top: 6px;
        }
      }
    }

    .signup-link {
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
    .law {
      padding: 24px 0;
      p {
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
