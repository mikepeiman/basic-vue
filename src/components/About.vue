<template>
  <div class="content">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      title: "About"
    };
  }
};
</script>

<style scoped>
.content {
  background: rgba(50,100,250,0.5);
  padding: 1em 0;
}
</style>

