<!-- tab切换 -->
<template lang="">
  <div>
    <el-tabs v-model="activeName">
      <el-tab-pane label="推荐" name="first">
        <MusicPage></MusicPage>
      </el-tab-pane>
      <el-tab-pane label="最新" name="second">最新</el-tab-pane>
    </el-tabs>
  </div>
</template>
<script>
import MusicPage from './MusicPage.vue';
export default {
  name: 'TabbarPage',
  components: {
    MusicPage
  },
  data() {
    return {
      activeName: 'first', // 默认选中tab
    }
  },
}
</script>
<style>
  
</style>