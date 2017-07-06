<template>
  <div class="selectLink">
    <select v-for="item in selects" :name="item">
      <option value="all">全部</option>
      <option value=""></option>
    </select>
  </div>
</template>

<style lang="less" scoped>
  select{
    margin: 0 20px;
  }
</style>
<script>
  export default {
    props: {
    	selects: {
    		type: Array,
        default: function(){
        	return ['provice','city','county']
        },
        data: {
        	type: Array
        }
      }
    },
    data() {
      return {}
    },
    methods: {},
    created() {

    },
    mounted() {
    },
    computed:{

    }
  }
</script>
