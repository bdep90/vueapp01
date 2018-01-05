<template>
  <div class="hello">
    <!-- {{ }} > display model data property -->
    <h1>{{ msg }}</h1>
    <div>
      <ul>
        <!-- render array of data -->
        <li v-for="user in users">
          {{ user.firstname }} {{ user.lastname }}
        </li>
      </ul>
    </div>
    <div>
      <!-- binding -->
      <input type="text" v-model="input_val">
    </div>
    <div>
      <!-- in place of {{ }} -->
      <span v-text="input_val"></span>
    </div>
    <div>
      <!-- click event + counter -->
      <button class="btn" v-on:click="counter++">You've clicked me {{counter}} times!</button>
    </div>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      users: [
        {firstname: 'Bridgette', lastname: 'Depay'},
        {firstname: 'Joan', lastname: 'Leslie'}
      ],
      input_val: '',
      counter: 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
div {
  padding: .25rem 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
