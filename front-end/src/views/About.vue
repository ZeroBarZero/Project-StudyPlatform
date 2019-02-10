<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button v-on:click="test_func">TEST</button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      test: ''
    }
  },
  methods: {
    test_func: function () {
      this.$http.post('/api/user/login',{id:'test', password:'1434'})
      .then((response) => {
        alert(response.data.message)
      })
    }
  },
  created () {
    this.$http.get('/api/user/login')
    .then((response) => {
      this.test = response.data
    })
  }
}
</script>