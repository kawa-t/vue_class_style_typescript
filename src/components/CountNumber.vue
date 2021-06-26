<template>
  <div>
    <AddButton @push="countUp"></AddButton>
    <Display :count="count"></Display>
  </div>
</template>
<script lang="ts">
import Componrnt from "vue-class-component";
import { Vue, Watch } from "vue-property-decorator";
import AddButton from "./Atoms/AddButton.vue";
import Display from "./Atoms/Display.vue";

@Componrnt({
  components: {
    AddButton,
    Display,
  },
})
export default class App extends Vue {
  public count = 0;
  public countUp(): void {
    this.count++;
  }
  @Watch("count", { immediate: true })
  public finishCount(newVal: number): void {
    if (newVal > 50) {
      alert("EndGame");
      this.count = 0;
    }
  }
}
</script>
