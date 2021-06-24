<template>
  <children :childTitle="title">AAAA</children>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Children from "./Child.vue";

@Component({
  components: {
    Children,
  },
})
export default class Parent extends Vue {
  public title = "parent to children";
}
</script>
