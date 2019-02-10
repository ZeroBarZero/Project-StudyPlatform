<template>
  <div class="auth-page">
    <div class="container page">
      <div class="row">
        <div class="col-md-6 offset-md-3 col-xs-12">
          <h1 class="text-xs-center">Sign up</h1>
          <p class="text-xs-center">
            <router-link :to="{ name: 'login' }">
              Have an account?
            </router-link>
          </p>
          <ul v-if="errors" class="error-messages">
            <li v-for="(v, k) in errors" :key="k">{{ k }} {{ v | error }}</li>
          </ul>
          <v-form v-on:submit.prevent="onSubmit">
            <v-flex class="form-group">
              <v-text-field
                class="form-control form-control-lg"
                type="text"
                v-model="username"
                placeholder="Username"
                required
              />
            </v-flex>
            <v-flex class="form-group">
              <v-text-field
                class="form-control form-control-lg"
                type="text"
                v-model="email"
                placeholder="Email"
                required
              />
            </v-flex>
            <v-flex class="form-group">
              <v-text-field
                class="form-control form-control-lg"
                type="password"
                v-model="password"
                placeholder="Password"
                required
              />
            </v-flex>
            <v-btn class="btn btn-lg btn-primary pull-xs-right">
              Sign up
            </v-btn>
          </v-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import { mapState } from "vuex";
//import { REGISTER } from "@/store/actions.type";
export default {
  name: "RwvRegister",
  data() {
    return {
      username: "",
      email: "",
      password: "",
      error : false
    };
  },
  /*computed: {
    ...mapState({
      errors: state => state.auth.errors
    })
  },
  methods: {
    onSubmit() {
      this.$store
        .dispatch(REGISTER, {
          email: this.email,
          password: this.password,
          username: this.username
        })
        .then(() => this.$router.push({ name: "home" }));
    }
  }*/
};
</script>