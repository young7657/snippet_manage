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
      <el-form ref="form" :model="form" label-width="80px">
        <el-form-item label="name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>

        <el-form-item label="language">
          <el-select v-model="form.language" placeholder="choose language">
            <el-option label="HTML" value="html"></el-option>
            <el-option label="JAVASCRIPT" value="javascript"></el-option>
          </el-select>
        </el-form-item>


        <el-form-item label="description">
          <el-input type="textarea" v-model="form.desc"></el-input>
        </el-form-item>

        <el-form-item label="content">
          <el-input type="textarea" v-model="form.content"></el-input>
        </el-form-item>
      </el-form>
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
      createVisible: false,
      form: {
        name: '',
        language: '',
        desc: '',
        content: ''
      }
    }
  },
  methods: {
    showCreateDialog() {
      console.log(111)
      this.createVisible = true
    },
    createDialogSure() {

    },
    onSubmit() {
      console.log('submit!');
    }
  }
}
</script>

<style scoped>

</style>
