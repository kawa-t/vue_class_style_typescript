<template>
  <div>
    <h3>Vue.extendで記述</h3>
    <button @click="pushExtend">Click Button(Extend.ver)</button>
  </div>
</template>
<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "AddButtonExtend",
  methods: {
    pushExtend(): void {
      this.$emit("push_extend");
    },
  },
});
</script>
