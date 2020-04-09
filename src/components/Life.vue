<template>
  <div>
    <h2>生命周期的</h2>
    <p v-if="isShow">{{str1}}</p>
    <p v-else>{{str2}}</p>
    <button class="btn" @click="stop">清除定时器</button>
  </div>
</template>

<script>
export default {
  beforeCreate () {
    console.log('1、初始化时，就已经创建了这个函数 beforeCreate（）')
  },
  data () {
    return {
      isShow: false,
      str1: '中国',
      str2: '美国'
    }
  },
  computed: {

  },
  created () {
    console.log('2、项目初始化完成时 created()')
  },
  beforeMounte () {
    console.log('3、开始编译')
  },
  mounted () {
    console.log('4、编译完成')
    // 定时器
    this.insterId = setInterval(() => {
      this.isShow = !this.isShow
      console.log('+++++++++++++++++++++++++++++++++++++')
    }, 1000)
  },
  watch: {

  },
  methods: {
    stop () {
      this.$destroy()
    }
  },
  components: {

  },
  beforeUpdate () {
    console.log('5、数据请求之前')
  },
  updated () {
    console.log('6、数据请求完成')
  },
  beforeDestroy () {
    console.log('7、组件销毁之前')
    clearInterval(this.insterId)
  },
  destroyed () {
    console.log('8、组件销毁')
  }

}
</script>

<style lang="scss" scoped>
</style>
