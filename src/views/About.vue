<template>
  <div class="about">
    <h1>This is an about page</h1>
    <el-button @click="visible = true">el-button</el-button>
    <el-dialog :visible.sync="visible" title="Hello world">
      <p>Try Element</p>
    </el-dialog>
  </div>
</template>
