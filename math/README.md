
## MathOther.cs
### 概要
- 数学関連のクラスです

### 関数
- `IsPrime`関数
    - 引数`num`が素数かどうかを調べます
        - 検索終了までの速度は *O( sqrt(n) / 6 )* です
<br></br>

- `Factorial`関数
    - 引数`num`番目の階乗の値を返します
<br></br>

- `Mersenne`関数
    - 引数`num`番目のメルセンヌ数を返します

<br></br>

## Round.cs
### 概要
- 丸め処理のクラスです

### 関数
- `Round`関数
    - 四捨五入した数値を返します
        > 第一引数`value`: 四捨五入する値  
        > 第二引数`place`: 桁指定（default: 0）

    ```C#
    int value = 182.351;
    Debug.Log(Round(value, 1));
    Debug.Log(Round(value, 0));
    Debug.Log(Round(value, -2));
    ```
    > \> 182.4  
    > \> 182  
    > \> 200

<br></br>

- `RoundUp`関数
    - 切り上げた数値を返します
        > 第一引数`value`: 切り上げる値  
        > 第二引数`place`: 桁指定（default: 0）

    ```C#
    int value = 182.351;
    Debug.Log(RoundUp(value, 1));
    Debug.Log(RoundUp(value, 0));
    Debug.Log(RoundUp(value, -2));
    ```
    > \> 182.4  
    > \> 183  
    > \> 200

<br></br>

- `RoundDown`関数
    - 切り捨てた数値を返します
        > 第一引数`value`: 切り捨てる値  
        > 第二引数`place`: 桁指定（default: 0）

    ```C#
    int value = 182.351;
    Debug.Log(RoundDown(value, 1));
    Debug.Log(RoundDown(value, 0));
    Debug.Log(RoundDown(value, -2));
    ```
    > \> 182.3  
    > \> 182  
    > \> 100