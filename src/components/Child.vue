<template>
  <div>
    <p>
      {{ Childtitle }}
    </p>
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Child extends Vue {
  @Prop()
  private Childtitle: string;
}
</script>
