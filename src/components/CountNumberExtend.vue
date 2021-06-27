<template>
  <div class="count__wrapper">
    <AddExButton @push_extend="countupExtend"></AddExButton>
    <PlayGoundEx :count_extend="count_extend"></PlayGoundEx>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import AddExButton from "./Atoms/AddButtonExtend.vue";
import PlayGoundEx from "./Atoms/PlayGoundExtend.vue";

export type DataType = {
  count_extend: number;
};

export default Vue.extend({
  name: "CountNumberExtend",
  components: {
    AddExButton,
    PlayGoundEx,
  },
  data(): DataType {
    return {
      count_extend: 0,
    };
  },
  methods: {
    countupExtend: function(): void {
      this.count_extend++;
    },
  },
  watch: {
    count_extend: function(CountNumerEx: number): void {
      if (CountNumerEx > 10) {
        alert("EndGame");
        this.count_extend = 0;
      }
    },
  },
});
</script>

<style>
button {
  margin: 10px;
  padding: 10px;
}
.count__wrapper {
  margin: 30px 100px;
}
</style>
