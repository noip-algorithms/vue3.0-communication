<template>
<h3>{{}}</h3>
  <son-component :msg="msg" @receive="handler"></son-component>
</template>

<script lang="ts">
import { defineComponent, ref} from 'vue'
import SonComponent from './components/SonComponent.vue'

export default defineComponent({
  name: 'App',
  components: {
    SonComponent
  },
  setup(): any {
    const msg: object = ref("朝饮木兰之坠露兮 夕餐秋菊之落英")
    function handler(value): void { console.log(value);
     }
   
    return { msg,handler }
  }
})
</script>

<style>
#app {
  text-align: center;
}
</style>
