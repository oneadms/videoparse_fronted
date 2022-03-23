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
import { onMounted,onBeforeMount } from '@vue/runtime-core'
export default {
  name: 'App',
  components:{
  mixin
  },
  setup(){
    onMounted(()=>{
      alert('hello')
      
    }),
    onBeforeMount(()=>{
      alert("达咩")
    })

    
   
  },
  data(){
    return{
      name:"hello"
    }
  },
 
  created(){
  }
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
