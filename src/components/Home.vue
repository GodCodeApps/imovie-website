<template>
  <div id="home">
    <div id="div">
      <div id="div-store">
        <div>
          <p style=" font-size:28px;color: white">爱电影客户端</p>
          <div>
            <img id="img-store" src="../assets/google-play.png" @click="openGooglePlay()">
            <img id="img-store" src="../assets/apk-zh.png" @click="openApkZh()">
            <img id="img-store" src="../assets/app-store.png" @click="openAppStore()">
          </div>
        </div>

      </div>

      <p style="font-size: 28px;color: black;font-weight: bold">关于爱电影(imovie)</p>
      <p style="font-size: 18px;color: black;">海量电影大片、影视、剧集、动漫、综艺、视频资源</p>
      <p id="p-gray">爱电影，众多热门新剧、经典老剧院线大片，韩剧、美剧、日剧、英剧、泰剧统统聚合搜罗，你想看的都在这里！
        强大搜索功能，剧好看在手，各种应有尽有！
        爱电影是一款视频聚合类产品，无论你是想看蓝光电影、热播电视剧、综艺、动漫、纪录片，这里通通都有！
        所有资源全球实时更新。
        众多热门电视剧院线大片统统免费观看，你想看的都在这里！
        爱电影是一款超火的视频聚合类产品，集多家正版影视资源于一身。无论是热播电视剧、高清电影、火热综艺、还是人气动漫，更有韩剧，美剧，日剧，泰剧，港剧，想看就看，千万部影片陪你欢度每一天。
        比影视大全还要片全！免费看片追剧一款就够了！ 【影视短视频】：挖掘宝藏国片，解读精彩电影，更新鲜更有趣 【万部大片在线点播】：汇聚国片经典、院线新片，与你分享最精彩的好电影
        【CCTV6电视同步】：电影频道节目同步直播收看，精彩永不错过 【精彩剧集】：爱情喜剧、家庭伦理、经典武侠、抗战史诗一网打尽 【高清电影直播】：24小时365天，永不打烊的移动影院
      </p>

      <div id="div-footer">
        <li><a href="http://124.222.242.16:8082/privacy.html" style="color: #999999">用户隐私政策</a></li>
        -->
      </div>
    </div>
    <!--    <h1>{{ msg }}</h1>-->
    <!--    <p>-->
    <!--      For a guide and recipes on how to configure / customize this project,<br>-->
    <!--      check out the-->
    <!--      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.-->
    <!--    </p>-->
    <!--    <h3>Installed CLI Plugins</h3>-->
    <!--    <ul>-->
    <!--      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank"-->
    <!--             rel="noopener">babel</a></li>-->
    <!--      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank"-->
    <!--             rel="noopener">eslint</a></li>-->
    <!--    </ul>-->
    <!--    <h3>Essential Links</h3>-->
    <!--    <ul>-->
    <!--      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>-->
    <!--      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>-->
    <!--      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>-->
    <!--      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>-->
    <!--      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>-->
    <!--    </ul>-->
    <!--    <h3>Ecosystem</h3>-->
    <!--    <ul>-->
    <!--      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>-->
    <!--      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>-->
    <!--      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a>-->
    <!--      </li>-->
    <!--      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>-->
    <!--      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>-->
    <!--    </ul>-->


  </div>
</template>

<script>

export default {
  name: 'SubTitle',
  props: {
    msg: String
  },
  methods: {
    openGooglePlay() {
      window.open('https://play.google.com/store/apps/details?id=com.github.imovie', "_blank")

    },
    openAppStore() {
      this.showToast("正在开发中，请耐心等待!")
    },
    openApkZh() {
      var a = document.createElement('a')
      a.download = name || 'apk'
      a.href = 'http://124.222.242.16:8080/file/others/app-release-20220401061258600.apk';
      a.click();
    },
    showToast(msg, duration) {
      duration = isNaN(duration) ? 3000 : duration;
      var m = document.createElement('div');
      m.innerHTML = msg;
      m.style.cssText = "width:50%; min-width:40px; background:#000; opacity:0.7; text-align:center; height:auto;min-height: 50px; color:#fff; line-height:50px; text-align:center; border-radius:4px; position:fixed; top:50%; left:20%; right:20%; z-index:999999;";
      document.body.appendChild(m);
      setTimeout(function () {
        var d = 0.5;
        m.style.webkitTransition = '-webkit-transform ' + d + 's ease-in, opacity ' + d + 's ease-in';
        m.style.opacity = '0';
        setTimeout(function () {
          document.body.removeChild(m)
        }, d * 1000);
      }, duration);
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#home {
  width: 100%;
  height: 100%;
  background-color: white;
}

#div {
  width: 100%;
  height: 30rem;
  background: url("../assets/body_bg.jpg");
}

#div-store {
  height: 100%;
  display: flex;
  align-items: center;
  margin-left: 120px;
}

#img-store {
  height: 40px;
  margin: 6px;
}

#p-gray {
  color: #656565;
  font-size: 0.32rem;
  line-height: 1.8;
  margin-right: 45px;
  margin-left: 45px;
}

#div-footer {
  width: 100%;
  height: 5.88rem;
  min-height: 150px;
  margin-top: 18rem;
  background-color: #0D1119;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
