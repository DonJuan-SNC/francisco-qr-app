<template>
  <div class="d-flex justify-center align-center" style="height: 100vh;">
    <v-card max-width="500">
      <v-card-text>
        <v-card-title class="justify-center">SIGN IN</v-card-title>
          <v-card-text>
            <v-form ref="form">
              <v-text-field
                label="Email"
                prepend-icon="mdi-email"
              ></v-text-field>
              <v-text-field
                label="Password"
                prepend-icon="mdi-lock"
              ></v-text-field>
            </v-form>
          </v-card-text>
        <!-- Log In Button -->
        <v-btn
          class="mb-4 mt-6"
          color="blue"
          size="large"
          variant="tonal"
          block
          @click="logIn"
        >
          Sign In
        </v-btn>
        

        <!-- Google Sign-In Button -->
        <v-btn
          class="mb-2"
          color="red"
          size="large"
          variant="tonal"
          block
          @click="signInWithGoogle"
        >
          Sign in with Google
        </v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<style>
.v-card {
  padding: 20px;
}
</style>

<script>
export default {
  layout: 'auth',
  middleware: 'guest',
  methods: {
    signInWithGoogle() {
      this.$auth.loginWith('google')
    }
  }
}
</script>