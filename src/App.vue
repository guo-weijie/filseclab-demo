<template>
  <div>
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import { useStore } from "vuex";
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
export default {
  components:{
      Header,
      Footer
  },
  setup(){
    const store=useStore()
    const setMode=()=>{
      let w=document.documentElement.clientWidth;
      if(w>960){
        store.state.client==='mobile'?store.commit('setWidth','pc'):null
        return
      }
      store.state.client==='pc'?store.commit('setWidth','mobile'):null
    }
    window.addEventListener('resize',setMode)
    return {

    }
  }  
}
</script>

<style lang="scss">

</style>
