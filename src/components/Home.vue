<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <AllConnections :friends="friends" @unfriend="remove" />
    <OnlineConnections :friends="friends" />
   
  </div>
</template>

<script>
import AllConnections from "./AllConnections";
import OnlineConnections from "./OnlineConnections";

export default {
  name: "Home",
  components: {
    AllConnections,
    OnlineConnections
  },
  data() {
    return {
      msg: "Welcome, Mike",
      friends: [
        { name: "Friend One", online: true },
        { name: "Friend Two", online: false },
        { name: "Friend Three", online: true },
        { name: "Friend Four", online: false }
      ]
    };
  },
  methods: {
    remove(thisIndex) {
      // typically this argument is named 'payload'
      console.log(thisIndex)
      this.friends = this.friends.filter((friend, index) => {
        return thisIndex.index !== index
        // this one originally, it works:
        // return (friend ? (thisIndex.index !== index) : none)
      })
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
  border-bottom: 1px solid rgba(0,0,0,0);
}
li:hover {
  border-bottom: 1px solid rgba(50,100,255,0.75);
  cursor: pointer;
}
a {
  color: #42b983;
}
</style>
