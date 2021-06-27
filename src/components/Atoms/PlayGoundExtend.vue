<template>
  <div>
    <p>you check button {{ count_extend }} times(Extend.ver)</p>
    <p>yout score : {{ doubleCount_exted }} points(Extend.ver)</p>
  </div>
</template>
<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "PlayGoundEx",
  props: {
    count_extend: Number,
  },
  computed: {
    doubleCount_exted(): number {
      return this.count_extend * 2;
    },
  },
});
</script>
