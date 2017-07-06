<template>
  <div class="index-wrapper">
    <div class="selects-wrapper">
      <select-link :selects="selects" :data="selectData"></select-link>
    </div>
    <div class="cbar-wrapper">
      <category-bar :data="barData" :option="barOptions"></category-bar>
    </div>
  </div>

</template>

<style lang="less" scoped>
  .index-wrapper {
    text-align: left;
  }

  .cbar-wrapper {
    width: 1000px;
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
        barOptions: {
          minWidth: 200,
          height: 60,
          childMinWidth: 30
        },
        barData: [
          {
            name: '未处理',
            value: 500,
            color: '#000',
            width: 0,
            children: [
              {
                name: '未响应',
                value: 200,
                color: '#bbb'
              },
              {
                name: '未下发',
                value: 300,
                width: 0,
                color: '#777'
              }
            ]
          },
          {
            name: '已处理',
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
      selectData: function () {
        var data = regions.slice(), ret = [];
        data.forEach((item) => {

        })
      }
    }
  }
</script>
