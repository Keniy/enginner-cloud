<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <vPagination :total="total" :current-page='current' :pagegroup="pagegroup" @pagechange="pagechange" v-if="isShowPagination"></vPagination>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      total: 1,
      current: 1,
      pagegroup: 10,
      isShowPagination: true
    }
  },
  methods: {
    pagechange (currentPage) {
      console.log('currentPage=', currentPage)
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
