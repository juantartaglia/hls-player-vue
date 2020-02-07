<template>
  <div id="app">
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
    <div class="player-container">
      <video-player ref="videoPlayer" :options="playerOptions"> </video-player>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data: () => {
    return {
      sources: [
        "https://bitdash-a.akamaihd.net/content/sintel/hls/playlist.m3u8",
        "http://184.72.239.149/vod/smil:BigBuckBunny.smil/playlist.m3u8",
        "http://playertest.longtailvideo.com/adaptive/bipbop/gear4/prog_index.m3u8"
      ],
      playerOptions: {
        overNative: false,
        autoplay: true,
        controls: false,
        width: 300,
        height: 200,
        techOrder: ["flash", "html5"],
        sourceOrder: false,
        html5: { hls: { withCredentials: false } },
        sources: [
          {
            withCredentials: false,
            type: "application/x-mpegURL",
            src:
              "http://playertest.longtailvideo.com/adaptive/bipbop/gear4/prog_index.m3u8"
          }
        ]
        // https://github.com/videojs/video.js/blob/master/docs/guides/options.md
        // controlBar: {
        //   timeDivider: false, // 时间分割线
        //   durationDisplay: false, // 总时间
        //   progressControl: true, // 进度条
        //   customControlSpacer: true, // 未知
        //   fullscreenToggle: true // 全屏
        // },
      }
    };
  }
};
</script>

<style>
.player-container {
  float: left;
  width: 300;
  height: 200;
}
</style>
