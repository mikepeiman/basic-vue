<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <AllConnections />
    <OnlineConnections />
   
  </div>
</template>

<script>
import AllConnections from './AllConnections'
import OnlineConnections from './OnlineConnections'

export default {
  name: 'Home',
  components: {
    AllConnections,
    OnlineConnections
  },
  data () {
    return {
      msg: 'Welcome, Mike'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
