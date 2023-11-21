
# 拡張メソッド(Expantion Method)
既存のデータ型やクラス等に新たな関数機能を追加するクラスです

<br></br>

## Boolean Expansion
### 概要
- bool型の拡張クラスです

### 関数
- `ToInt`関数
    - bool型のプロパティをint型の 0, 1 に変換します

    ```C#
    bool flag = true;
    Debug.Log(flag.ToInt() * 5);
    ```
    > \> 5

<br></br>

- `Random`関数
    - 一定の確率でtrueを返す関数です
        > 第一引数`rate`: trueを返す確率（0.0 to 1.0）

<br></br>

## Color Expansion
### 概要
- Color型の拡張クラスです

### 関数
- `ToHex`関数
    - RGB値をカラーコードで取得
        > 第一引数`isUpper`: アルファベットは大文字か（default: `true`）

    ```C#
    Debug.Log(Color.red.ToHex());
    ```
    > \> #FF0000FF

<br></br>

- `GetAlphaColor`関数
    - アルファ値を変更したColorを返します
        > 第一引数`a`: 変更するアルファ値

    ```C#
    Debug.Log(Color.red.GetAlphaColor(0.5f));
    ```
    > \> Color(1.0, 0.0, 0.0, 0.5)

<br></br>

- `GetHue`関数
    - 色相を返します

    ```C#
    // シアン(水色)
    Debug.Log(Color.cyan.GetHue());
    ```
    > \> 0.5

<br></br>

- `GetSaturation`関数
    - 彩度を返します

    ```C#
    // 灰色
    Debug.Log(Color.gray.GetSaturation());
    ```
    > \> 0

<br></br>

- `GetValue`関数
    - 明度を返します

    ```C#
    // 灰色
    Debug.Log(Color.gray.GetSaturation());
    ```
    > \> 0.5

<br></br>

- `SetHSV`関数
    - HSVを変更した色を返します
        > 第一引数`h`: 色相の設定値（省略可能）  
        > 第一引数`s`: 彩度の設定値（省略可能）  
        > 第一引数`v`: 明度の設定値（省略可能）

    ```C#
    Debug.Log(Color.red.GetAlphaColor(0.5f));
    ```
    > \> Color(1.0, 0.0, 0.0, 0.5)

<br></br>

- `Contrast`関数
    - コントラストを変動させた色を返します
        > 第一引数`contrast`: 変動倍率（default: 1）

    ```C#
    Debug.Log(Color.red.GetAlphaColor(0.5f));
    ```
    > \> Color(1.0, 0.0, 0.0, 0.5)

<br></br>

- `GetRelativeColor`関数
    - 均等に離れた色相の色を配列で返します
        > 第一引数`num`: 配列の要素数

    ```C#
    Color[] colors = Color.red.GetRelativeColor(4);

    foreach(Color color in colors)
        Debug.Log(color.GetHue());
    ```
    > \> 0  
    > \> 0.25  
    > \> 0.5  
    > \> 0.75

<br></br>

## Enum Expansion
### 概要
- 列挙型に関する拡張クラスです

### 関数
- `AtRandom`関数
    - 指定された列挙型の中からランダムな列挙子を返します
<br></br>

- `GetLength`関数
    - 列挙型の要素数を返します

<br></br>

## GameObject Expansion
### 概要
- GameObjectの拡張クラスです

### 関数
- `GetOrAddComponent`関数
    - コンポーネントを取得します
    - コンポーネントがない場合はアタッチして返します
<br></br>

- `SetLayer`関数
    - 自分自身のレイヤーを変更します
    > 第一引数`layer`: 設定するレイヤー番号・レイヤー名
    > 第二引数`setChildren`: 子オブジェクトのレイヤーも変更するか

<br></br>

## List Expansion
### 概要
- リストの拡張クラスです

### 関数
- `AtRandom`関数
    - リスト内のランダムな要素を返します
<br></br>

- `Shuffle`関数
    - リストの中身をシャッフルします
<br></br>

- `IsProtrude`関数
    - インデックスが配列外かどうかをbool型で返します
    > 第一引数`index`: 調べるインデックス

<br></br>

## Numeric Expansion
### 概要
- 数値型の拡張クラスです

### 関数
- `Digit`関数
    - 数値の桁数を返します
    ```C#
    Debug.Log((141592).Digit());
    ```
    > \> 6

<br></br>

- `FormatSize`関数
    - 制限: long型
    - 値をSI接頭語によって簡略化したフォーマット形式にします
        > 第一引数`isUpper`: アルファベットを大文字にするか
    ```C#
    Debug.Log((1263000).FormatSize());
    ```
    > \> 1.26M

<br></br>

## String Expansion
### 概要
- string型の拡張クラスです

### 関数
- `Repeat`関数
    - 指定回数繰り返した文字列を返します
    ```C#
    stinrg text = "Repeat";
    Debug.Log(text.Repeat(3));
    ```
    > \> RepeatRepeatRepeat

<br></br>

- `HitCount`関数
    - 検索文字列のヒット回数を返します
        > 第一引数`search`: 検索する文字列

    ```C#
    stinrg text = "This text as contain data here.";
    Debug.Log(text.HitCount("ta"));
    ```
    > \> 2

<br></br>

- `ExtractNumerics`関数
    - 数値を抽出します
    - 見つからなかった場合、NaNを返します

    ```C#
    stinrg text = "Index -1234.5678";
    Debug.Log(text.ExtractNumerics());
    ```
    > \> -1234.5678

<br></br>

- `GetLine`関数
    - 行で区切った時の指定行目の文字列を抽出します
        - 第一引数のみ
        > 第一引数`line`: 指定行
        - 第二引数付き
        > 第一引数`startLine`: 指定開始行  
        > 第二引数`endLine`: 指定終了行

<br></br>

- `ToFullWidth`関数
    - 半角の英数字を全角にします
<br></br>

- `ToHalfWidth`関数
    - 全角の英数字を半角にします


<br></br>

## Transform Expansion
### 概要
- Transformの拡張クラスです

### 関数
- `GetChildren`関数
    - 自分自身に含まれる全ての子オブジェクトを非再帰的に取得します
    - 孫以降の子々孫々も取得したい場合は、以下の関数を用いてください
    ```C#
    transform.GetComponentsInChildren<Transform>()
    ```

<br></br>

- `GetRootParent`関数
    - 最上位の親を取得します

<br></br>

## Vector Expansion
### 概要
- ベクトルの拡張クラスです

### 関数
- `Offset`関数
    - 個々の軸で一定距離離れたベクトルを返します
    > 第一引数`x`: x軸のオフセット（default: 0）  
    > 第二引数`y`: y軸のオフセット（default: 0）  
    > 第三引数`z`: z軸のオフセット（default: 0）

<br></br>

- `Setter`関数
    - 個々の軸を変更したベクトルを返します
        - 引数がnullの軸は変更しません
    > 第一引数`x`: x軸の変更後の値（default: null）  
    > 第二引数`y`: y軸の変更後の値（default: null）  
    > 第三引数`z`: z軸の変更後の値（default: null）

<br></br>
- `GetSwapXY`関数: x軸とy軸を入れ替えたベクトルを返します
- `GetSwapXZ`関数: x軸とy軸を入れ替えたベクトルを返します
- `GetSwapYZ`関数: x軸とy軸を入れ替えたベクトルを返します
