# インターフェース

インターフェースは、クラスと異なり実体を持たない(`new`を利用してインスタンスを生成できない)。

 * 宣言のみ可能
  * メソッドの宣言のみ可能。メソッドの実装は、インターフェースを`implements`したクラスに記述する。
 * すべて`public`
  * メンバー（フィールド・メソッド）は必ず`public`になる。`public`の記述は省略可能。
 * 状態を持たない
  * フィールドは`public static final`となり、値の変更が不可能となる。
 
クラスでは`implements`キーワードで、実装するインターフェースを宣言する。

```java
interface SampleInterface {
  // この記述はpublic finalが適用される
  String CONST = "変数は定義できない";

  String method(); // メソッドは宣言のみ可能
  
  // ※Java 8から：defaultで実体を持つメソッドの定義が可能に
  default String defaultMethod() {
    return "Java8の機能";
  }
}

class SampleClass implements SampleInterface {

  @Override
  public String method() { // インターフェースで宣言されたメソッドの実装が必須となる
    ...
  }

}
```