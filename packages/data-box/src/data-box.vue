<template>
  <div class="data-box">
    <el-row :span="24">
      <el-col :span="span"
              v-for="(item,index) in data"
              :key="index">
        <div class="item">
          <div class="item-icon"
               :style="{backgroundColor:item.color}">
            <i :class="item.icon"></i>
          </div>
          <div class="item-info">
            <h3 :style="{color:item.color}">{{item.count}}</h3>
            <p>{{item.title}}</p>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'AvueDataBox',
  data () {
    return {
      span: this.option.span || 6,
      data: this.option.data || [],
    }
  },
  props: {
    option: {
      type: Object,
      default: () => { }
    }
  },
  created () { },
  mounted () { },
  watch: {},
  computed: {},
  methods: {}
}
</script>

<style lang="scss" scoped>
</style>
