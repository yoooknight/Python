<template>
    <div style="margin-bottom: 30px;display: flex;justify-content: center;align-items: center; width:200px;">
        <el-input>
            @keyup.enter.native="searchBlick"
            placeholder = "通过书名或作者搜索..."
            size="small"
            style="width: 400px;margin-right: 10px"
            v-model="keywords"
        </el-input>
        <el-button size="small" type="primary" icon="el-icon-search" @click="searchClick" style="margin-left:10px">
            搜索
        </el-button>
    </div>
</template>

<script>
export default {
  name: 'SearchBar',
  data () {
    return {
      keywords: '',
      books: [],
      cardLoading: []
    }
  },
  methods: {
    searchClick () {
      this.$emit('onSearch')
    }
  }
}
</script>

<style scoped>

</style>
