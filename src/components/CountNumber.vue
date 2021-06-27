<template>
  <div class="count__wrapper">
    <AddButton @push="countUp"></AddButton>
    <PlayGound :count="count"></PlayGound>
  </div>
</template>
<script lang="ts">
import Component from "vue-class-component";
import { Vue, Watch } from "vue-property-decorator";
import AddButton from "./Atoms/AddButton.vue";
import PlayGound from "./Atoms/PlayGound.vue";

@Component({
  components: {
    AddButton,
    PlayGound,
  },
})
export default class App extends Vue {
  public count = 0;
  public countUp(): void {
    this.count++;
  }
  @Watch("count")
  public finishCount(CountNumer: number): void {
    if (CountNumer > 10) {
      alert("EndGame");
      this.count = 0;
    }
  }
}
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
