<template>
  <div class="dashboard-container">
    <el-form ref="form" :model="form" label-width="120px">
      <div class="hnp">
        <el-form-item label="h1:">
          <el-input v-model="form.h1"></el-input>
        </el-form-item>
        <el-form-item label="n1:">
          <el-input v-model="form.n1"></el-input>
        </el-form-item>
        <el-form-item label="p1:">
          <el-input v-model="form.p1"></el-input>
        </el-form-item>
        <el-form-item label="h2:">
          <el-input v-model="form.h2"></el-input>
        </el-form-item>
        <el-form-item label="n2:">
          <el-input v-model="form.n2"></el-input>
        </el-form-item>
        <el-form-item label="p2:">
          <el-input v-model="form.p2"></el-input>
        </el-form-item>
      </div>
      <el-form-item label="protein:">
        <el-input type="textarea" :autosize="{ minRows: 4, maxRows: 10}" v-model="form.proteinDesc"></el-input>
      </el-form-item>
      <el-form-item label="window size:">
        <el-select v-model="form.windowSize" placeholder="choose">
          <el-option
            v-for="item in sizeOptions"
            :key="item.value"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="name:">
        <el-input v-model="form.name"></el-input>
      </el-form-item>
      <el-form-item label="email:">
        <el-input v-model="form.email"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit" style="float: right;margin: 2%;">submit</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  data() {
    return {
      form: {
        proteinDesc: '',
        windowSize: '',
        name: '',
        email: '',
        h1: '',
        n1: '',
        p1: '',
        h2: '',
        n2: '',
        p2: ''
      },
      sizeOptions: [
        { value: 1,label: 1 },{ value: 2,label: 2 },{ value: 3,label: 3 },{ value: 4,label: 4 },{ value: 5,label: 5 },
        { value: 6,label: 6 },{ value: 7,label: 7 },{ value: 8,label: 8 },{ value: 9,label: 9 },{ value: 10,label: 10 }
      ]
    }
  },
  methods: {
    onSubmit() {

    }
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}

.hnp {
  .el-form-item {
    display: inline-block;
  }
}
</style>
