<template>
  <div class="container">
    <!-- <test :name="name" hello="true" >

      <template  v-slot:slot1>
        <div >
          <p slot:slot1="日你妈退钱">老子就是你的爹</p>
          <div class="row"></div>
          <div class="row"></div>
          <div class="row"></div>
        </div>
      </template>
           <template  v-slot:slot2>
        <div >
          <p>222</p>
        </div>
      </template>

  </test> -->
    <mixin></mixin>

  </div>
</template>

<script>
// import test from '@/components/test'
import mixin from '@/components/mixin'
import {
  onMounted,
  onBeforeMount,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
  onActivated,
  onDeactivated,
  onErrorCaptured,
  reactive,
} from '@vue/runtime-core'
export default {
  name: 'App',
  components: {
    mixin,
  },
  setup() {
   
    /**
     * onBeforeMount——挂载开始前调用
onMount——挂载后调用
onBeforeUpdate——当响应数据改变，且重新渲染前调用
onUpdated——重新渲染后调用
onBeforeUnmount——Vue实例销毁前调用
onUnmounted——实例销毁后调用
onActivated——当keep-alive组件被激活时调用
onDeactivated——当keep-alive组件取消激活时调用
onErrorCaptured——从子组件中捕获错误时调用
     */
    // 生命周期 钩子 写在一块  形成一片独立的流程 看起来更加清晰
    onBeforeMount(() => {
      alert('1')
    }),
      onMounted(() => {
        alert('2')
       
      }),
      onBeforeUpdate(() => {
        alert('3')
      }),
      onUpdated(() => {
        alert('4')
      }),
      onBeforeUnmount(() => {
        alert('5')
      }),
      onUnmounted(() => {
        alert('6')
      }),
      onActivated(() => {
        alert('7')
      }),
      onDeactivated(() => {
        alert('8')
      }),
      onErrorCaptured(() => {
        alert('9')
      })
  },
  data() {
    return {
      name: "hello"
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
