<template>
  <v-footer
     height="auto"
     color="primary lighten-1">
    <v-layout
     justify-center
     row
     wrap>
      <router-link class="logo-font" :to="{ name: 'home', params: {} }">
        study365
      </router-link>
      <v-flex class="attribution">
        An interactive learning project from
        <a rel="noopener noreferrer" target="blank" href="https://thinkster.io"
          >Thinkster</a>. Code &amp; design licensed under MIT.
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  name: "RwvFooter"
  
};
</script>
