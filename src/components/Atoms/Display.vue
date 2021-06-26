<template>
  <div>
    <p>you check button {{ count }} times</p>
    <p>yout score : {{ doubleCount }} points</p>
  </div>
</template>
<script lang="ts">
import Component from "vue-class-component";
import { Prop, Vue } from "vue-property-decorator";

@Component
export default class Display extends Vue {
  @Prop()
  public count!: number;

  public get doubleCount(): number {
    return this.count * 2;
  }
}
</script>
