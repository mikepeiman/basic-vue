<template>
  <div class="content">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "SignIn",
  data() {
    return {
      title: "SignIn"
    };
  }
};
</script>

<style scoped>
.content {
  background: rgba(250,100,150,0.5);
  padding: 1em 0;
}
</style>

