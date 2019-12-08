<template>
  <div class="home">
    <Header></Header>
    <Aside></Aside>
    <Main></Main>
  </div>
</template>

<script>
// @ is an alias to /src

import Header from '@/components/Header.vue'
import Aside from '@/components/Aside.vue'
import Main from '@/components/Main.vue'
export default {
  name: 'home',
  components: {
    Header,
    Aside,
    Main

  }
}
</script>
