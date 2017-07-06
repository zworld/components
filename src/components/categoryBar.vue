<template>
  <div class="wrapper" ref="wrapper">
    <div class="bar"
         v-for="item in data"
         :style="{ background: item.color, height: option.height + 'px', width: item.width + 'px'}">

    </div>
  </div>
</template>

<style lang="less" scoped>
  .wrapper {
    width: 100%;
  }

  .bar {
    float: left;
    position: relative;
  }

  .bar-children {
    position: absolute;
    height: 100%;
    left: 0;
    right: 0;
    top: 100%;

  }
</style>
<script>
  export default {
    data() {
      return {}
    },
    props: {
      data: [Array],
      option: [Object]
    },
    methods: {
    	setWidths() {
        var _this = this;
        var parentWidth = $('.wrapper').parent().width();
        var values = this.data.map((item) => {
          return item.value
        })
        var count = values.reduce((pre,cur) => {return pre + cur})
        var minWidth = this.option.minWidth;
        var widths = values.map((value)=>{
        	return parentWidth * value / count
        })
        widths.forEach((width)=>{
        	_this.data.forEach((item)=>{
        		item.width = width
            console.log(width)
          })
        })

      }
    },
    created() {



    },
    mounted() {
      var vm = this;
      vm.setWidths.call(vm)

    }
  }
</script>
