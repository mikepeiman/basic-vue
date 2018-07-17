<template>
  <div id="all-friends">
    <h2>All Friends</h2>
    <div id="all-friends-list">
      <li @click="unfriend(index)" v-for="(friend, index) in friends" :key="index" class="li-connection">
        {{index}}, {{ friend.name }}
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: "AllConnections",
  props: ['friends'],
  data() {
    return {
    };
  },
  methods: {
    unfriend(index) {
      this.$emit('unfriend', { index })
    }
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

