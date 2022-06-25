<template>
  <div id="header">
    <img id="img-logo" src="../assets/logo.png">
    <h3>爱电影</h3>
    <h5 style="width: 90%;text-align: end;margin-right: 25px" onclick="contactWe()">联系我们</h5>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  methods: {
    contactWe() {

    }

  }
}
</script>

<style scoped>
#header {
  width: 100%;
  height: 5rem;
  display: flex;
  background-color: white;
  align-items: center;
  justify-content: space-between;
}

#img-logo {
  width: 50px;
  height: 50px;
  margin-left: 25px;
}
</style>