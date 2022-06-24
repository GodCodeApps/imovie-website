<template>
  <div id="header">
    <img id="img-logo" src="../assets/logo.png">
    <h3>爱电影</h3>
    <h5 style="width: 90%;text-align: end">联系我们</h5>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header"
}
</script>

<style scoped>
#header {
  width: 100%;
  height: 5rem;
  display: flex;
  padding-left: 2rem;
  padding-right: 2rem;
  flex-direction: row;
  background-color: white;
  align-items: center;
}

#img-logo {
  width: 50px;
  height: 50px;
  margin-right: 15px;
}
</style>