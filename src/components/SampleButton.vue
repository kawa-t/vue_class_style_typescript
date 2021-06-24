<template>
  <div class="hello">
    <h1>aaa</h1>
    <h1>{{ massage }}</h1>
    <p>{{ saySomething() }}</p>
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop()
  private massage!: string;

  saySomething(): string {
    const something = "something";
    return something;
  }
}
</script>
