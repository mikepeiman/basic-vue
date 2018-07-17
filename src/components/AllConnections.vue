<template>
  <div id="all-friends">
    <h2>All Friends</h2>
    <div id="all-friends-list">
      <li v-for="(friend, index) in friends" :key="index" class="li-connection">
        {{ friend.name }}
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: "All Connections",
  data() {
    return {
      friends: [
        { name: "Friend One", online: true },
        { name: "Friend Two", online: false },
        { name: "Friend Three", online: true },
        { name: "Friend Four", online: false }
      ]
    };
  }
};
</script>

<style>
#all-friends-list, #online-friends-list {
  display: flex;
  flex-direction: column;
  margin-left: 40vw;
}
.li-connection {
  align-self: flex-start;
  /* justify-self: center; */
  /* display: block; */
  /* background: blue; */
}
</style>

