<!-- 歌曲组件 -->
<template>
  <div>
    <div class="music-container">
      <div class="music-content-container" @mouseenter="handleMouseEnter(dataObj)"  @mouseleave="handleMouseLeave(dataObj)">
        <img width="100%" height="100%" src="../../../static/img/1.png" alt="加载失败">
        <span class="time-container">0.333333</span>
        <div class="icon-container" v-if="dataObj.show">
          <i class="iconfont iconfont-container icon-caiyouduo_gendanxiangqing-fenxiang"></i>
          <i class="iconfont iconfont-container icon-bofang2"></i>
          <i class="iconfont iconfont-container icon-jia"></i>
        </div>
      </div>
      <router-link to="">海底</router-link><br>
      <router-link to="" style="font-size: 13px; color: #4d4b4b;">一只榴莲</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MusicPage',
  props: {
    dataObj: {
      type: Object,
      default() {
        return {
          show: false
        }
      }
    }
  },
  data() {
    return {
      iconIsShow: false
    }
  },
  methods: {
    /**
     * 鼠标移出
     * @param {*} item 
     */
    handleMouseLeave(item) {
      // item.show = true
      item.show = false
    },
    /**
     * 鼠标移入
     * @param {*} item 
     */
    handleMouseEnter(item) {
      item.show = true
    }
  }
}
</script>
<style scoped>
.music-container {
  width: 162px;
  height: 215px;
  margin: 0;
  display: inline-block;
  /* border: 1px solid; */

}
.music-content-container {
  width: 160px;
  height: 160px;
  margin-bottom: 10px;
  border: 1px solid #f5f5f5;
  border-radius: 8px 8px;
  overflow: hidden;
  position: relative;
  text-align: center;
}
.time-container {
  font-size: 13px;
  color: #ffffff;
  position: absolute;
  bottom: 5px;
  right: 5px;
}
.icon-container {
  width: 100%;
  height: 30px;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
  position: absolute;
  top: calc(50% - 15px);
  color: #c0c0c0;
}
.iconfont-container {
  font-size: 30px;
}
</style>