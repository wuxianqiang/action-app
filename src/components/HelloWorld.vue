<template>
  <div @click="handleClick">{{msg}}</div>
</template>

<script>
export default {
  data () {
    return {
      obj: { a: '1' },
      arr: [1,2,3]
    }
  },
  created () {
    console.log(this.obj)
    this.$watch('obj', (newVal) => {
      console.log(newVal)
    }),
    this.$watch('arr', (newVal) => {
      console.log(newVal)
    })
  },
  methods: {
    handleClick () {
      console.log('点击')
      this.obj.a = Math.random()
      this.arr.push(Math.random())
    }
  },
  setup () {
    return {
      msg: 'hello'
    }
  }
}
</script>

<style>

</style>


