<template>
  <div>
    <h3>{{msg}}</h3>
    <button @click="send">Child Pass Data</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: "SonComponent",
  props: {
    msg: { type: String, required: true}
  },
  setup(props,ctx): any{
    const send = ():void => {
      ctx.emit('receive','朝饮木兰之坠露兮 夕餐秋菊之落英')
    }
    return {send}
  }
})
</script>

<style scoped>

</style>
