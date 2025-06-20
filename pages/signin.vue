<template>
    <div class="d-flex justify-center align-center" style="height: 100vh;">
        <v-card max-width="500">
          <v-card-title class="justify-center">Login</v-card-title>
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
          <v-btn block
          color="primary">
            SIGNIN
         </v-btn>
         <v-btn block
          color="primary">
            SIGNIN
         </v-btn>
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
    layout: "auth",
}
</script>