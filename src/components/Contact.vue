<template>
  <div class="content">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      title: "Contact"
    };
  }
};
</script>

<style scoped>
.content {
  background: rgba(50,200,150,0.5);
  padding: 1em 0;
}
</style>

