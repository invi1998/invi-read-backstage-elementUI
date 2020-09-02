 <!--  -->
<template>
  <el-row class="tac">
    <el-col :span="12">
      <el-menu
        default-active="1-1"
        background-color="#545c66"
        text-color="#fff"
        active-text-color="#ffd0cc"
        mode="vertical"
        unique-opened
        :collapse="isCollapse"
        :collapse-transition="false"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
        @select="handleSelect"
      >
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-location" />
            <span>导航一</span>
          </template>
          <el-menu-item-group>
            <template slot="title">分组一</template>
            <el-menu-item index="1-1">选项1-1</el-menu-item>
            <el-menu-item index="1-2">选项1-2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group>
            <template slot="title">分组二</template>
            <el-menu-item index="2-1">选项2-1</el-menu-item>
            <el-menu-item index="2-2">选项2-2</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="1-4">
            <template slot="title">选项1-4</template>
            <el-menu-item index="1-4-1">选项1</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <i class="el-icon-menu" />
            <span slot="title">导航二</span>
          </template>
          <el-menu-item index="2-1">选项2-1</el-menu-item>
        </el-submenu>
        <el-menu-item index="3" disabled>
          <i class="el-icon-document" />
          <span slot="title">导航三</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting" />
          <span slot="title">导航四</span>
        </el-menu-item>
      </el-menu>
    </el-col>
    <el-col>
      <el-button @click="isCollapse = !isCollapse">折叠菜单栏</el-button>
    </el-col>
  </el-row>
</template>

<script>
//  这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//  例如：import 《组件名称》 from '《组件路径》';

export default {
  //  import引入的组件需要注入到对象中才能使用
  components: {},
  data() {
    // 这里存放数据
    return {
      isCollapse: false
    }
  },
  // 监听属性 类似于data概念
  computed: {},
  // 监控data中的数据变化
  watch: {},
  // 生命周期 - 创建完成（可以访问当前this实例）
  created() {},
  // 生命周期 - 挂载完成（可以访问DOM元素）
  mounted() {},
  beforeCreate() {}, // 生命周期 - 创建之前
  beforeMount() {}, // 生命周期 - 挂载之前
  beforeUpdate() {}, // 生命周期 - 更新之前
  updated() {}, // 生命周期 - 更新之后
  beforeDestroy() {}, // 生命周期 - 销毁之前
  destroyed() {}, // 生命周期 - 销毁完成
  activated() {},
  // 方法集合
  methods: {
    handleSelect(key, keypath) {
      console.log('handleSelect', key, keypath)
    },
    handleOpen(key, keypath) {
      console.log('handleSelect', key, keypath)
    },
    handleClose(key, keypath) {
      console.log('handleSelect', key, keypath)
    }
  } // 如果页面有keep-alive缓存功能，这个函数会触发
}
</script>
<style lang='scss' scoped>
//@import url(); 引入公共css类
</style>
