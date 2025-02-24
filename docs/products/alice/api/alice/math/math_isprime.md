---
title: math_isPrime
summary: 指定した数値が素数であるかを表す値を取得します。
---

### 定義
名前空間: Alice.Math<br/>
アセンブリ: Losetta.Runtime.dll<br/>
ソースコード: [Alice.Math.cs](https://github.com/WSOFT-Project/Losetta/blob/master/Losetta.Runtime/Alice.Math.cs)

#### math_isPrime(number)

指定した数値が素数であるかを表す値を取得します。

```cs title="AliceScript"
namespace Alice.Math;
public bool math_isPrime(number value);
```

|引数| |
|-|-|
|`value`|判定対象の数値。|

|戻り値| |
|-|-|
|`number`|`value`が素数であれば`true`、それ以外の場合は`false`。|

???note "対応: AliceScript RC1以降"
    |対応||
    |---|---|
    |AliceScript|RC1、RC2、GM、2.0、2.1、2.2、2.3、3.0|
    |AliceSister|GM、2.0、2.1、2.2、2.3、3.0|
    |Losetta|0.8、0.9、0.10|

### 説明
素数は、`1`とその数自身のみを約数に持つ数と定義されています。

`value`の値が[math_NaN](./math_nan.md)、[math_Infinity](./math_infinity.md)、[math_NegativeInfinity](./math_negativeinfinity.md)または`2`未満の数の場合、この関数は`false`を返します。

### 例
次の例では、一桁の自然数のうち、素数のものを表示しています。

```cs title="AliceScript"
using Alice.Math;

for(var n = 0;n < 10; n++)
{
    if(math_isPrime(n))
    {
        print(n);
    }
}
```