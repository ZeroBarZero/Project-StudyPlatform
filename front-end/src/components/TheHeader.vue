
<template>
  <v-toolbar>
    <v-menu offset-y>
    <v-toolbar-side-icon  slot="activator" ></v-toolbar-side-icon>
    <v-list>
        <v-list-tile
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-menu>
    <v-toolbar-title>
      <router-link class="navbar-brand" :to="{ name: 'home' }">
        study365
      </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
      <v-toolbar-items  v-if="!1" class="hidden-sm-and-down">
        <v-btn flat >Link One</v-btn>
        <v-btn flat>Create </v-btn>
        <v-btn flat>Logout</v-btn>
      </v-toolbar-items>
      <v-toolbar-items v-else class="hidden-sm-and-down">
        <v-btn flat>Link One</v-btn>
        <v-btn flat to="/create">Create</v-btn>
        <v-btn flat to="/login" exact>Login</v-btn>
      </v-toolbar-items> 
  </v-toolbar>
</template>

<script>
//import { mapGetters } from "vuex";
export default {
  name: "RwvHeader",
  data: () => ({
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' }
      ]
    })
  /*computed: {
    ...mapGetters(["currentUser", "isAuthenticated"])
  }*/
};
</script>