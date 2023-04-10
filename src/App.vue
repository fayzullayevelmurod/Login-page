<template>
  <v-app>
    <div class="background"></div>
    <v-main class="d-flex justify-center align-center">
      <v-col cols="11" md="8" lg="4" class="mx-auto">
        <v-card class="pa-4">
          <div class="text-center">
            <v-avatar size="100" color="yellow lighten-2">
              <v-icon size="60" class="yellow">mdi-account</v-icon>
            </v-avatar>
            <h2 class="grey--text">Login Page</h2>
          </div>
          <v-form>
            <v-card-text>
              <v-text-field
                type="email"
                label="Email"
                placeholder="Email"
                prepend-inner-icon="mdi-account"
              />
              <v-text-field
                :type="passwordShow?'text':'password'"
                label="Password"
                placeholder="Password"
                prepend-inner-icon="mdi-key"
                :append-icon="passwordShow ? 'mdi-eye':'mdi-eye-off'"
                @click:append="passwordShow = !passwordShow"
              />
              <v-switch label="Remember me" color="yellow"></v-switch>
            </v-card-text>
            <v-card-actions class="justify-center">
              <v-btn color="yellow">
                <span class="grey--text px-8">Login</span>
              </v-btn>
            </v-card-actions>
          </v-form>
        </v-card>
      </v-col>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    passwordShow:false, 
  }),
};
</script>

<style scoped>
.background{
  background-image: url('./assets/bgs.jpg');
  height: 500px;
  width: 100%;
  display: block;
  position: absolute;
  top: 0;
  background-size: cover;
}
</style>
