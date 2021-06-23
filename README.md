#### vue_class_style_typescript

Vue.extend を使わないもう一つの方法

```
import { Component, Vue } from "vue-property-decorator"

@Component({

})
```

型推論ができているのにアノテーションつけるとエラー出る

> Type string trivially inferred from a string literal, remove type annotation (no-inferrable-types)
> string（型推論）いらない

```
export default class Home extends Vue {
  public greetText: string = "Hello";
}
```
