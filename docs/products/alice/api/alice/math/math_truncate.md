---
title: math_truncate
summary: 指定した数値の整数部を取得します
---

### 定義
名前空間: Alice.Math<br/>
アセンブリ: Losetta.Runtime.dll<br/>
ソースコード: [Alice.Math.cs](https://github.com/WSOFT-Project/Losetta/blob/master/Losetta.Runtime/Alice.Math.cs)

#### math_truncate(number)

指定した数値の整数部を取得します。

```cs title="AliceScript"
namespace Alice.Math;
public number math_truncate(number value);
```

|引数| |
|-|-|
|`value`|切り捨てたい対象の数値|

|戻り値| |
|-|-|
|`number`|`value`の整数部|

???note "対応: AliceScript RC1以降"
    |対応||
    |---|---|
    |AliceScript|RC1、RC2、GM、2.0、2.1、2.2、2.3、3.0|
    |AliceSister|GM、2.0、2.1、2.2、2.3、3.0|
    |Losetta|0.8、0.9、0.10|

### 説明
この関数は、`value`を0に向かってもっとも近い整数に丸めます。

また、`value`の値が[math_NaN](./math_nan.md)の場合、この関数は[math_NaN](./math_nan.md)を返します。さらに、`value`の値が正負どちらかの無限の場合、この関数は無限を返します。

小数部を切り上げたいときは[math_celling](./math_celling.md)を、四捨五入したいときは[math_round](./math_round.md)を使用してください。

### 例
次の例では、いくつかの数の小数部を切り捨てています。

```cs title="AliceScript"
using Alice.Math;

print(math_truncate(12.3));  //出力 : 12
print(math_truncate(-12.3)); //出力 : -12
```