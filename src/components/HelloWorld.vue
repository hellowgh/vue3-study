<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- <el-button type="primary">向父组件传值</el-button> -->
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from 'vue'

/**
 * 1、通过props接收(接口 + 泛型)
 */
// 定义接口
interface Props {
  msg?: string
}

// 通过泛型定义props
defineProps<Props>()

/**
 * 2、向父组件传递数据（发布订阅者模式）
 */
const emit = defineEmits(['changeMsg'])

emit('changeMsg')
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
