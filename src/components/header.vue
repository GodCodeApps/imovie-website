<template>
  <div id="header">
    <img id="img-logo" src="../assets/logo.png">
    <h3 style="width: auto;margin-left: 8px">爱电影</h3>
    <div id="div-contact-we">
      <h5 style="position: absolute;right: 25px; top: 10px" @mouseenter="contactWe"
          @click="contactWe">联系我们</h5>
      <div id="tl" v-if="isShow">
        <a href="https://jq.qq.com/?_wv=1027&k=CVmTOViF">QQ交流群:665754684</a>
        <a style="margin-top: 4px" href="https://ptcc.in/joinchat/1RmE94AsKtVQQFwx1WmzuA">Potato交流群</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "header",
  data() {
    return {
      isShow: false
    }
  },
  methods: {
    contactWe() {
      this.isShow = !this.isShow
    },
  }
}
</script>

<style scoped>
#header {
  width: auto;
  height: 5rem;
  display: flex;
  padding-right: 25px;
  padding-left: 25px;
  background-color: white;
  align-items: center;
}

#img-logo {
  width: 50px;
  height: 50px;
  align-self: center;
}

#div-contact-we {
  text-align: center;
  align-items: center;
}

#tl {
  width: auto;
  height: auto;
  top: 60px;
  right: 0;
  display: flex;
  text-align: start;
  flex-direction: column;
  visibility: visible;
  padding: 20px;
  border-radius: 0px 0px 10px 10px;
  position: absolute;
  background-color: white;
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
}

</style>