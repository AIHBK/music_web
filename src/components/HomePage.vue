<template>
  <div>
    <tagPage :tagList="tagList"></tagPage>
    <router-view></router-view>
  </div>
</template>

<script>
import tagPage from '@/components/Tag/TagPage.vue'
export default {
  name: 'HomePage',
  components: {
    tagPage,
  },
  props: {
  },
  data() {
    return {
      tagList: [
        {
          tagName: 'test23333333333',
          path: '/home/tag'
        },
        {
          tagName: 'test',
          path: '123'
        },
        {
          tagName: 'test',
          path: '123'
        },
        {
          tagName: 'test',
          path: '123'
        },
        {
          tagName: 'test',
          path: '123'
        },
      ]
    }
  },
}
</script>
<style scoped>

</style>
