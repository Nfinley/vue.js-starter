<template>
  <div id="app">

    <input type="text" v-model="msg">
    <label for="myInfo">
      <input
              type="checkbox"
              id="myInfo"
              @click="simpleAlert"
              v-model="profile.preference" />
      My info
    </label>
    <span :class="{red: profile.preference}">{{ profile.preference }}</span>

    <span v-show="profile.preference"> I am shown when true  </span>
    <h4>
      <span :class="{red: !profile.preference}" v-show="!profile.preference"> I am shown when false  </span>

    </h4>
      <Header
          :message="msg">
      </Header>



    <img src="./assets/logo.png">
    <h1></h1>
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      profile: {
      	preference: true
      }
    }
  },
  components: {
  	Header
  },
  methods: {
  	simpleAlert() {
  		alert('are you sure dude?');
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  }

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

.red {
  color: red;
}

</style>
