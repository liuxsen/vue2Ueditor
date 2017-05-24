<template>
    <div class="edit-area">
      <ueditor v-bind:value=defaultMsg v-bind:config=config v-on:input="input" v-on:ready="ready"></ueditor>
    </div>
</template>

<script>
import ueditor from './vueUditor'
export default {
  name: 'hello',
  data () {
    return {
      defaultMsg: '初始文本',
      config: {
        initialFrameWidth: null,
        initialFrameHeight: 200,
      }
    }
  },
  components: {
    ueditor
  },
  methods: {
    ready(editorInstance){
      console.log(editorInstance)
    },
    input(obj){
        console.log(obj);
    }
  },
  mounted(){
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
