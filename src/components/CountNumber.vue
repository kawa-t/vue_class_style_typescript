<template>
  <div>
    <AddButton @push="countUp"></AddButton>
    <Display :count="count"></Display>
  </div>
</template>
<script lang="ts">
import Componrnt from "vue-class-component";
import { Vue } from "vue-property-decorator";
import AddButton from "./components/Atoms/AddButton.vue";
import Display from "./components/Atoms/Display.vue";

@Componrnt({
  components: {
    AddButton,
    Display,
  },
})
export default class App extends Vue {}
</script>
