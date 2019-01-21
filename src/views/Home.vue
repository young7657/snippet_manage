<template>
  <div class="home">
    <div>
      <el-button
        type="primary"
        icon="el-icon-plus"
        @click="showCreateDialog">Create</el-button>
    </div>
    <el-row class="tac">
      <el-col :span="6">
        <h3>Language</h3>
        <el-menu
          default-active="1"
          class="el-menu-vertical-demo">
          <el-menu-item index="1">
            <i class="el-icon-menu"></i>
            <span slot="title">分类一</span>
          </el-menu-item>
          <el-menu-item index="2">
            <i class="el-icon-document"></i>
            <span slot="title">分类二</span>
          </el-menu-item>
          <el-menu-item index="3">
            <i class="el-icon-setting"></i>
            <span slot="title">分类三</span>
          </el-menu-item>
        </el-menu>
      </el-col>
    </el-row>

    <el-dialog
      title="Create"
      :visible.sync="createVisible"
      width="600px">
      <span>这是一段信息</span>
      <span slot="footer" class="dialog-footer">
        <el-button @click="createVisible = false">Cancel</el-button>
        <el-button type="primary" @click="createDialogSure">Sure</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      createVisible: false
    }
  },
  methods: {
    showCreateDialog() {
      console.log(111)
      this.createVisible = true
    },
    createDialogSure() {

    }
  }
}
</script>

<style scoped>

</style>
