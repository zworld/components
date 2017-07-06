<template>
  <div class="index-wrapper">
    <select-link :selects="selects" :data="selectData"></select-link>
  </div>
</template>

<style lang="less" scoped>
  .index-wrapper{
    text-align: left;
  }
</style>
<script>
    import SelectLink from 'components/selectLink'
    import regions from 'lib/china_regions/region_dumps.json'

    export default {
        components: {
          SelectLink
        },
        data() {
            return {
            	selects: ['province', 'city', 'country'],
            }
        },
        methods: {},
        created() {

        },
        mounted() {
        	console.log($)
        },
        computed: {
        	//value label children格式
          selectData: function(){
          	var data = regions.slice(),ret=[];
          	data.forEach((item) => {

            })
          }
        }
    }
</script>
