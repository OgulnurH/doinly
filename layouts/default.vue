<template>
  <div class="main">
   <div class="header" v-if="path == '/'">
    <Header />
   </div>
    <nuxt />
  </div>
</template>

<script>
import Header from '@/components/header.vue'
import path from 'path';
export default {
  name: 'DefaultLayout',
  components: {
    Header,
  },
  data() {
    return {}
  },
  computed:{
    path(){
      return this.$route.path;
    }
  }
}
</script>
