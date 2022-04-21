<template>
  <div>
<h2>Bonjour</h2>
<h2>Bonjour</h2>
    <NuxtLink to="/shahin">Shahin page</NuxtLink>
  </div>
</template>

<script>
export default {
  name: "MoreFunIndex",
  mounted(){
    console.log("lmklm")
    const items = []
    this.$router.options.routes.forEach(route => {
      items.push({
        name: route.name
        , path: route.path
      })
    })
    console.log(items)
  }

}
</script>

<style scoped>

</style>
