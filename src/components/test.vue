<template>
  <div class="wrapper">{{name}}

    <slot   name="slot1"></slot>
    <slot  name="slot2"></slot>
  </div>
</template>

<script>
export default {
  components: {},

  props: {
    name: {
      type: String,
    },
  },
  
  // 父组件传递
  // context 里面 包含了 属性 attrs 和slots 插槽
  // context 是一个普通的 JavaScript 对象，也就是说，它不是响应式的，这意味着你可以安全地对 context 使用 ES6 解构。
  setup(props, context) {
    alert(JSON.stringify(props))
    alert(JSON.stringify(context))
    
  },
  data() {
    return {}
  },
  watch: {},
  computed: {},
  methods: {},
  created() {},
  mounted() {},
}
</script>
<style scoped>
.wrapper {
}
</style>