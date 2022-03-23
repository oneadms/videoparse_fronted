<template>
  <div>
    {{msg}}
  </div>
</template>
<script>
// 合并两个参数的值 相同属性取自身
import {mixin} from '../mixin/index'
export default {
  mixins:[mixin],
  data(){
    return {

      msg:'world'
    }
  },
  created() {
    console.log(JSON.stringify(this.$data));
  },
}
</script>
<style>
  
</style>