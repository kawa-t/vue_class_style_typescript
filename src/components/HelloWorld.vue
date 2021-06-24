<template>
  <div class="hello">
    <div class="home">
      <MyButton :greet="greetText"></MyButton>
      <parent-page />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import MyButton from "./SampleButton.vue";
import ParentPage from "./Parent.vue";

@Component({
  name: "Home",
  components: {
    MyButton,
    ParentPage,
  },
})
export default class Home extends Vue {
  public greetText = "Hello";
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
