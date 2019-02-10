
<template>
  <nav class="navbar navbar-light">
    <div class="container">
      <router-link class="navbar-brand" :to="{ name: 'home' }">
        study365
      </router-link>
      <ul v-if="!1" class="nav navbar-nav pull-xs-right">
        <li>로그인 안함</li>
      </ul>
      <ul v-else class="nav navbar-nav pull-xs-right">
        <li>로그인 함</li>
      </ul>
    </div>
  </nav>
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