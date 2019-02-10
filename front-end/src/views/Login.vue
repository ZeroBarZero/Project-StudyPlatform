<template>
  <div class="auth-page">
    <div class="container page">
      <div class="row">
        <div class="col-md-6 offset-md-3 col-xs-12">
          <h1 class="text-xs-center">Sign in</h1>
          <p class="text-xs-center">
            <router-link :to="{ name: 'register' }">
              Need an account?
            </router-link>
          </p>
          <ul v-if="errors" class="error-messages">
            <li v-for="(v, k) in errors" :key="k">{{ k }} {{ v | error }}</li>
          </ul>
          <v-form v-on:submit.prevent="onSubmit(email, password);">
            <v-flex class="form-group">
              <v-text-field
                class="form-control form-control-lg"
                type="text"
                v-model="email"
                placeholder="Email"
              />
            </v-flex>
            <v-flex class="form-group">
              <v-text-field
                class="form-control form-control-lg"
                type="password"
                v-model="password"
                placeholder="Password"
              />
            </v-flex>
            <v-btn class="btn btn-lg btn-primary pull-xs-right">
              Sign in
            </v-btn>
          </v-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import { mapState } from "vuex";
//import { LOGIN } from "@/store/actions.type";
export default {
  name: "login",
  data() {
    return {
      email: null,
      password: null
    };
  },
  /*methods: {
    //onSubmit(email, password) {
      //this.$store
        //.dispatch(LOGIN, { email, password })
        //.then(() => this.$router.push({ name: "home" }));
    }
  },
  computed: {
    //...mapState({
      //errors: state => state.auth.errors
    })
  }*/
};
</script>