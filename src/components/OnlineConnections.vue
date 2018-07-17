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
  name: 'Online Connections',
  data() {
    return {
            friends: [
        { name: "Friend One", online: true },
        { name: "Friend Two", online: false },
        { name: "Friend Three", online: true },
        { name: "Friend Four", online: false }
      ]
    }
  }
}
</script>

<style scoped>

</style>

