<script setup lang="ts">
import { inject } from 'vue';
import type { TimeFormItem } from '@/views/form/index';

const configInfo: TimeFormItem = inject<TimeFormItem>("selectFormItem") as TimeFormItem;

</script>
<template>
  <div>
    <el-divider content-position="center">基础配置</el-divider>
    <el-form-item label="字段名">
      <el-input v-model="configInfo.field" maxlength="99" />
    </el-form-item>
    <el-form-item label="标签名">
      <el-input v-model="configInfo.label"></el-input>
    </el-form-item>
    <el-form-item label="默认值">
      <el-input v-model="configInfo.value" />
    </el-form-item>
    <el-form-item label="提示信息">
      <el-input v-model="configInfo.toolTip"></el-input>
    </el-form-item>
    <el-divider content-position="center">属性配置</el-divider>
    <el-form-item label="是否必填">
      <el-switch v-model="configInfo.required" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-form-item label="禁用">
      <el-switch v-model="configInfo.props.disabled" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-form-item label="文本框可输入">
      <el-switch v-model="configInfo.props.editable" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-form-item label="是否显示清除按钮">
      <el-switch v-model="configInfo.props.clearable" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-form-item label="非范围选择时的占位内容">
      <el-input v-model="configInfo.props.placeholder" maxlength="99" />
    </el-form-item>
    <el-form-item label="范围选择时开始时间的占位内容">
      <el-input v-model="configInfo.props.startPlaceholder" maxlength="99" />
    </el-form-item>
    <el-form-item label="范围选择时结束时间的占位内容">
      <el-input v-model="configInfo.props.endPlaceholder" maxlength="99" />
    </el-form-item>
    <el-form-item label="是否为时间范围选择">
      <el-switch v-model="configInfo.props.isRange" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-form-item label="是否使用箭头进行时间选择">
      <el-switch v-model="configInfo.props.arrowControl" inline-prompt active-text="是" inactive-text="否" />
    </el-form-item>
    <el-divider content-position="center">验证规则</el-divider>
    <el-form-item label="字段类型">
      <el-select v-model="configInfo.validate"></el-select>
    </el-form-item>
  </div>
</template>
<style scoped lang="scss">

</style>
