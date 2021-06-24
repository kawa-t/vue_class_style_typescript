<template>
  <div>
    <AddButton @push="countUp"></AddButton>
    <Display :count="count"></Display>
  </div>
</template>
<script lang="ts">
import Componrnt from "vue-class-component";
import { Vue } from "vue-property-decorator";

@Componrnt({})
export default class App extends Vue {}
</script>
