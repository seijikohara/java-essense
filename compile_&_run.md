# Javaのコンパイルと実行

## サンプルのソースファイル

`public static void main(String[] args)`メソッドがエントリポイントとなる。

```java
// ファイル名 Sample.java ※クラス名と一致する必要あり
public class Sample {
  // このメソッドがエントリポイント
  public static void main(String[] args) {
    System.out.println("Hello Java!");
  }
}
```

## コンパイル

コンパイルは`javac`コマンドを利用する。コンパイルを行うと`class`ファイルが生成される。

```shell
javac Sample.java
```

## 実行

実行は、`java`コマンドでエントリポイントをもつクラスを指定する。

```shell
java Sample
```