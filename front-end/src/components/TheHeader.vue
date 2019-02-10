
<template>
  <v-toolbar>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title>
      <router-link class="navbar-brand" :to="{ name: 'home' }">
        <v-toolbar-title>
        study365
        </v-toolbar-title>
      </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
      <v-toolbar-items  v-if="!1" class="hidden-sm-and-down">
        <v-btn flat>Link One</v-btn>
        <v-btn flat>Link Two</v-btn>
        <v-btn flat>Link Three</v-btn>
      </v-toolbar-items>
      <v-toolbar-items v-else class="hidden-sm-and-down">
        <v-btn flat>로그인 안함</v-btn>
      </v-toolbar-items> 
  </v-toolbar>
</template>

<script>
//import { mapGetters } from "vuex";
export default {
  name: "RwvHeader",
  /*computed: {
    ...mapGetters(["currentUser", "isAuthenticated"])
  }*/
};
</script>