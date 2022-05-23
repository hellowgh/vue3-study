<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>

<!-- 如果插槽不起名字，默认命名为default，可以有多个 -->
  <slot></slot>
  <slot>默认值</slot>

<!-- 具名插槽（多个插槽共存时，进行区分） -->
    <div>
        <slot name="header">
            <div>header</div>
        </slot>
    </div>
    <div>
        <slot name="footer">
            <div>footer</div>
        </slot>
    </div>

  <br v-for="item of 5" :key="item"/>
  4r4
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

/**
 * 1、通过props接收（Vue2延续的写法）
 */
const props = defineProps({
  msg: {
    type: String, // 规定类型
    required: true, // 是否必须
    // defult: '你好 Vue',
    default: () => '你好 Vue' // 默认值（如果是数组、对象等复杂数据类型，必须用函数返回）
  }
})
console.log(props.msg)

</script>

<style scoped>
</style>
