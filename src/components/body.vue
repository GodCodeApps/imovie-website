<template>
  <div id="home">
    <div id="div">
      <div id="div-store">
        <div>
          <p style=" font-size:28px;color: white">爱电影客户端</p>
          <div>
            <img id="img-store" src="../assets/google-play.png" @click="openGooglePlay()">
            <img id="img-store" src="../assets/apk-zh.png" @click="openApkZh()">
            <img id="img-store" src="../assets/app-store.png" @click="openAppStore()" style="visibility: hidden">
          </div>
        </div>
      </div>

      <p style="font-size: 28px;color: black;font-weight: bold">关于爱电影(imovie)</p>
      <p style="font-size: 18px;color: black;">海量电影、电视剧、动漫、综艺、每日更新</p>
      <p id="p-gray">爱电影，众多热门新剧、经典老剧院线大片，韩剧、美剧、日剧、英剧、泰剧统统聚合搜罗，你想看的都在这里！
        强大搜索功能，剧好看在手，各种应有尽有！
        爱电影是一款视频聚合类产品，无论你是想看蓝光电影、热播电视剧、综艺、动漫、纪录片，这里通通都有！
        所有资源全球实时更新。
        众多热门电视剧院线大片统统免费观看，你想看的都在这里！
        爱电影是一款超火的视频聚合类产品，集多家正版影视资源于一身。无论是热播电视剧、高清电影、火热综艺、还是人气动漫，更有韩剧，美剧，日剧，泰剧，港剧，想看就看，千万部影片陪你欢度每一天。
        比影视大全还要片全！免费看片追剧一款就够了！ 【影视短视频】：挖掘宝藏国片，解读精彩电影，更新鲜更有趣 【万部大片在线点播】：汇聚国片经典、院线新片，与你分享最精彩的好电影
        【CCTV6电视同步】：电影频道节目同步直播收看，精彩永不错过 【精彩剧集】：爱情喜剧、家庭伦理、经典武侠、抗战史诗一网打尽 【高清电影直播】：24小时365天，永不打烊的移动影院
      </p>


    </div>
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
      a.href = 'http://124.222.242.16:8080/file/others/app-mainland-official-release-20220713040710835.apk';
      a.click();
    },
    showToast(msg, duration) {
      duration = isNaN(duration) ? 3000 : duration;
      var m = document.createElement('div');
      m.innerHTML = msg;
      m.style.cssText = "width:50%; min-width:40px; background:#000; opacity:0.7; text-align:center; height:auto;min-height: 50px; color:#fff; line-height:50px; text-align:center; border-radius:4px; position:fixed; top:50%; left:20%; right:20%; z-index:999999; font-size: medium;";
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
  margin-left: 2rem;

}

#img-store {
  height: 40px;
  margin: 0.4rem;
}

#p-gray {
  color: #656565;
  font-size: 0.32rem;
  line-height: 1.8;
  padding-left: 1rem;
  padding-right: 1rem;
}
</style>
