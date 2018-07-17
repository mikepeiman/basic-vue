<template>
  <div id="online-friends">
    <h2>Online Friends</h2>
        <div id="online-friends-list">
      <li v-for="(friend, index) in friends" :key="index" class="li-connection" v-if="friend.online">
        {{ friend.name }}
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OnlineConnections',
  props: ['friends'],
  data() {
    return {
    }
  }
}
</script>

<style scoped>

</style>

