<template>
  <div>
    <div class="tag-container">
      <!-- <div > -->
        <router-link
         v-for=" (item, index) in tagList"
         :key="index" :to="item.path"
         class="tag-item-container"
         active-class="link-active"
        >
          {{ item.tagName }}
        </router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TagPage',
  props: {
    tagList: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      
    }
  },
}
</script>
<style scoped>
  .tag-container {
    width: 100%;
    height: auto;
  }
  .tag-item-container {
    min-width: 50px;
    text-align: center;
    padding: 5px;
    border: 1px solid #c0c0c0;
    border-radius: 40px;
    font-size: 13px;
    display: inline-block;
    margin: 5px;
  }
  .link-active {
    background: #fd353f;
    border: 1px solid #fd353f;
    color: #ffffff;
  }
  a {
    text-decoration:none;
    color:#000000;
  }
</style>