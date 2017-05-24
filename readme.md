+ [下载](http://ueditor.baidu.com/build/build_down.php?n=ueditor&v=1_4_3_3-utf8-php)
ueditor 源码包 放入 static目录下
+ 修改 ueditor.config.js 

```js
var URL = '/static/utf8-php/' || getUEBasePath();
```
+ 下载 vueUditor vue组件包放入components 目录下

+ 用法

```vue.js
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
```
