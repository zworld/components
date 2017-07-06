<template>
  <div class="wrapper" ref="wrapper">
    <div class="bar" v-for="item in data" :style="{ background: item.color }">

    </div>
  </div>
</template>

<style lang="less" scoped>
  .wrapper{
    width: 100%;
    overflow: hidden;
  }
  .bar{
    float: left;
  }
</style>
<script>
	export default {
		data() {
			return {}
		},
		props: {
			data: [Array],
      minWidth: [Number]
    },
		methods: {

    },
		created() {

		},
		mounted() {
			var vm = this;
			var el = vm.$el;
			console.log(el)
			console.log()
		}
	}
</script>
