<template>
  <div class="index-wrapper">
    <div class="selects-wrapper">
      <select-link :selects="selects" :data="selectData"></select-link>
    </div>
    <div class="cbar-wrapper">
      <category-bar :data="barData"></category-bar>
    </div>
  </div>

</template>

<style lang="less" scoped>
  .index-wrapper{
    text-align: left;
  }
  .cbar-wrapper{
    width: 500px;
  }
</style>
<script>
    import SelectLink from 'components/selectLink'
    import CategoryBar from 'components/categoryBar'
    import regions from 'lib/china_regions/region_dumps.json'

    export default {
        components: {
          SelectLink,
          CategoryBar
        },
        data() {
            return {
            	selects: ['province', 'city', 'country'],
              barOption: {
            		minWidth: 200,
                Height: 60
              },
              barData:[
                {
                	label: '未处理',
                  value: 500,
                  color: '#000'
                },
                {
                  label: '已处理',
                  value: 500,
                  color: '#f00'
                }
              ],
            }
        },
        methods: {},
        created() {

        },
        mounted() {
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
