<template>
  <div>
    <h3>クラスコンポーネントで記述</h3>
    <button @click="push">Click Button</button>
  </div>
</template>
<script lang="ts">
import Component from "vue-class-component";
import { Emit, Vue } from "vue-property-decorator";

@Component
export default class AddButton extends Vue {
  @Emit("push")
  public push(): void {
    // no return
  }
}
</script>
