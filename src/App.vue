<template>
  <div>
    <el-container>
    <!-- 菜单 start -->
    <div style="width: 200px; overflow: hidden; border-right: 1px solid #f5f5f5;">
      <el-aside width="218px" style="height: calc(100vh - 10px);">
        <img class="logo-container" src="../static/img/logo.png" alt="加载失败">
        <el-menu
          :router="true"
          :default-active="$route.path + '/tag'"
          style="margin-top: 120px;"
        >
          <el-menu-item v-for="item in menubarPersonList" :key="item.id" :index="item.path" style="position: relative;">
            <span slot="title">{{ item.title }}</span>
            <i :class="item.icon"></i>
          </el-menu-item>
          <div class="line-container"></div>
          <el-menu-item v-for="item in menubarSongList" :key="item.id" :index="item.path" style="position: relative;">
            <span slot="title">{{ item.title }}</span>
            <i :class="item.icon"></i>
          </el-menu-item>
          <div class="line-container"></div>
          <el-menu-item v-for="item in menubarList" :key="item.id" :index="item.path" style="position: relative;">
            <span slot="title">{{ item.title }}</span>
            <i class="menu-icon-container" :class="item.icon"></i>
          </el-menu-item>
        </el-menu>
      </el-aside>
    </div>

    <!-- 菜单 end -->
    <el-container>
      <!-- 导航 start -->
      <el-header class="Header-container">Header</el-header>
      <!-- 导航 end -->
      <!-- 内容 start -->
      <el-main>
        <div class="main-container">
          <router-view></router-view>
        </div>
      </el-main>
      <!-- 内容 end -->
      <!-- 底部 start -->
      <el-footer>Footer</el-footer>
      <!-- 底部 end -->
    </el-container>
  </el-container>
  </div>
</template>

<script>
// import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    // HomePage
  },
  data() {
    return {
      menubarPersonList: [
        {
          id: '1-1',
          title: '首页',
          path: '/home',
          icon: 'el-icon-star-on',
        },
        {
          id: '1-2',
          title: '随便听听',
          path: '',
          icon: 'el-icon-star-on',
        },
      ],
      menubarSongList: [
        {
          id: '2-1',
          title: '我的收藏',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '2-2',
          title: '我的关注',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '2-3',
          title: '我的歌单',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '2-4',
          title: '历史播放',
          path: '',
          icon: 'el-icon-star-on',
        },
      ],
      menubarList: [
        {
          id: '1',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '2',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '3',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '4',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '5',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '6',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '7',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '8',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '9',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },

        {
          id: '10',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '11',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '12',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '13',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '14',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '15',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '16',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '17',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '18',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
        {
          id: '19',
          title: '首页',
          path: '',
          icon: 'el-icon-star-on',
        },
      ]
    }
  },
  created() {
    console.log('----', this.$router);
  },
}
</script>

<style src="../static/iconfont/iconfon.css"></style>
<style>
body {
  margin: 0 !important;
}
.logo-container {
  width: 200px;
  height: 115px;
  position: fixed;
  z-index: 100;
}
.el-menu-item {
  height: 40px;
  line-height: 40px;
}
.menu-icon-container {
  font-size: 20px;
  position: absolute;
  right: 15px;
  top: 18px;
}
.Header-container {
  background: #f5f5f5;
}
.line-container {
  width: 180px;
  border-top: 1px solid #f5f5f5;
  margin: 10px auto;
}
.main-container {
  width: 65vw;
  height: 100%;
}
a {
    text-decoration:none;
    color:#000000;
  }
</style>
