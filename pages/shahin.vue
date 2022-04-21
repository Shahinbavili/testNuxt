<template>
<div>
  <p class="red">Hello World !</p>
  <button @click="count++">Count is: {{ count }}</button>
</div>
</template>

<script>
export default {
  head() {
    // Set meta tags for this page
  },
  name: "ShahinPage",
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style scoped>
button {
  font-weight: bold;
}
.red {
  color: red;
}
</style>
