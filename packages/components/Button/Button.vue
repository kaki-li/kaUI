<template>
  <el-button :type="type" :loading="loading" :disabled="disabled">
    <slot>{{ label }}</slot>
  </el-button>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import { ElButton } from "element-plus";

export default defineComponent({
  name: "MyButton",
  props: {
    type: {
      type: String as PropType<
        "primary" | "success" | "danger" | "info" | "warning"
      >,
      default: "primary",
    },
    label: {
      type: String,
      default: "点击我",
    },
    loading: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style scoped>
/* 可以在这里添加按钮的样式 */
</style>
