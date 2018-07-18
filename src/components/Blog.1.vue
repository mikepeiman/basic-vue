<template>
  <div class="content">
    <div id="blog">
      <h2>{{ blog.title }}</h2>
      <button @click="changeTitle">Change Title</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Blog',
  data() {
    return {
      blog: {
        title: 'Blog One',
        body: 'Writing is cool'
      }
    }
  },
  methods: {
    changeTitle() {
      if(this.blog.title === 'Blog One') {
        this.blog.title = 'Amazing JS magic'
      } else if(this.blog.title === 'Amazing JS magic')
      this.blog.title = 'Blog One'
    }
  },
  beforeCreate() {
    alert('beforeCreate hook fired')
  },
  created() {
    alert('created hook fired')
  },
  beforeUpdate() {
    alert('beforeUpdate hook fired')
  }
}
</script>
