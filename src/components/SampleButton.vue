<template>
  <div>
    <button @click="onClick">ボタン</button>
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class MyButton extends Vue {
  @Prop()
  public greet?: string;

  public onClick(): void {
    alert(this.greet);
  }
}
</script>
