<template>
    <div class="container">
    <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="120px" class="demo-ruleForm">
  <el-form-item label="First Name" prop="name1">
    <el-input v-model="ruleForm.name1"></el-input>
  </el-form-item>
  <el-form-item label="Last Name" prop="name2">
    <el-input v-model="ruleForm.name2"></el-input>
  </el-form-item>
  <el-form-item label="Email" input="email" prop="email">
    <el-input v-model="ruleForm.email"></el-input>
  </el-form-item>
  <el-form-item label="Subject Line" prop="subjectline">
    <el-input v-model="ruleForm.subjectline"></el-input>
  </el-form-item>
  <el-form-item label="Message" prop="desc">
    <el-input type="textarea" v-model="ruleForm.desc"></el-input>
  </el-form-item>
  <el-form-item label="Rules and Conditions" prop="type">
    <el-checkbox-group v-model="ruleForm.type">
      <el-checkbox label="Do you agree?" name="type"></el-checkbox>
    </el-checkbox-group>
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="submitForm('ruleForm')">Create</el-button>
    <el-button @click="resetForm('ruleForm')">Reset</el-button>
  </el-form-item>
</el-form>

<el-dialog
  title="Tips"
  :visible.sync="dialogVisible"
  width="30%"
  :before-close="handleClose">
  <span>This is a message</span>
  <span slot="footer" class="dialog-footer">
    <el-button @click="dialogVisible = false">Cancel</el-button>
    <el-button type="primary" @click="dialogVisible = false">Confirm</el-button>
  </span>
</el-dialog>
    </div>
</template>

<script src="./myform.js"></script>

<style src="./myform.css" scoped></style>