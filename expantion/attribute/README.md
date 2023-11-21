
# 属性(Attribute)
インスペクタービューでのプロパティ表示に変化をもたらすクラスです

```C#
[Min(0)]
[System.Serializable]
[RequireComponent(typeof(SpriteRenderer))]
```
標準では以上のような属性が存在し、各括弧でくくりプロパティの宣言前に指定することで稼働します

<br></br>

## Chapter Attribute
### 概要
- プロパティの上に区切り線を描画します
> 第一引数`chapterName`: 線の中に表示する文字列（省略で線のみに可能）  
> 第二引数`space`: 線の描画する際に上のプロパティとどれだけの間隔をあけるか

### プレビュー
```C#
[Chapter("コンポーネント")]
[SerializeField] Image m_ItemImage;
[SerializeField] Text m_ItemNameText;
[SerializeField] Text m_ItemQtyText;
[SerializeField] GameObject m_PlayerObject;
```
![Chapter](https://github.com/Woskni/Woskni/assets/103394833/ff64ded9-4c18-4358-9cde-ec939dd31cc0)


<br></br>

## Comment Attribute
### 概要
- プロパティの上にコメントを描画します
> 第一引数`comment`: コメントとして表示する文字列  
> 第二引数`space`: 線の描画する際に上のプロパティとどれだけの間隔をあけるか

### プレビュー
```C#
[SerializeField] int m_DataIndex;

[Comment("Assets/~ のファイルパス")]
[SerializeField] string m_DataPath;
[SerializeField] string m_NotFoundText;
```
![Comment](https://github.com/Woskni/Woskni/assets/103394833/96dca7f3-dfce-4adc-8051-fcca334afdc4)

<br></br>

## FilePath Attribute
### 制限
- string型

### 概要
- ディレクトリの選択でファイルパスをプロパティに設定できるようにします
- ディレクトリ選択はプロパティの右部から設定可能です
> 第一引数`pathType`: ファイルパスの開始位置  
> 第二引数`delimiter`: ファイルパスの区切り文字（デフォルトでは`/`）

### プレビュー
```C#
[FilePath(FilePathType.AssetsPath)]
[SerializeField] string m_DataPath;
```
[!] ここに **FilePathAttribute** の画像を設定

<br></br>

## MethodButton Attribute
### 概要
- クリックすることで関数を実行するボタンを描画します
> 第一引数`method`: 実行する関数名  
> 第二引数`buttonTitle`: ボタンに表示する文字列

- 引数はstringの配列で、複数の要素を設定すると水平方向に複数のボタンを描画します

### プレビュー
```C#
[MethodButton(new string[] {"AddHP"}, new string[] {"HP加算"})]
public int hp;
```
[!] ここに **MethodButtonAttribute** の画像を設定

<br></br>

## NameAttribute
### 概要
- エディタ上に表示するラベルの文字内容を変更します
> 第一引数`label`: 表示名

### プレビュー
```C#
[Name("再生成の所要時間")]
[SerializeField] int m_RegenerateDuration;
```
[!] ここに **NameAttribute** の画像を設定

<br></br>

## PreviewTexture Attribute
### 制限
- Sprite型
- Texture型
- Texture2D型

### 概要
- 画像をプレビュー表示します
> 第一引数`scaleX`: 横方向の拡大率  
> 第二引数`scaleY`: 縦方向の拡大率  
> 第一引数`aspectType`: アスペクト比の保持設定を種別する列挙型`AspectRatioType`  
>> 列挙型`AspectRatioType`の列挙子  
>> `None`: 標準の枠に収める  
>> `FixedInFrame`: 枠内でアスペクト比を固定する  
>> `AllFixed`: 枠による制御を受けずアスペクト比を固定する  

### プレビュー
```C#Sprite
[PreviewTexture(aspectType = AspectRatioType.AllFixed)]
public Sprite m_Sprite;

[PreviewTexture(aspectType = AspectRatioType.AllFixed)]
public Texture[] m_Textures;
```
[!] ここに **PreviewTextureAttribute** の画像を設定

<br></br>

## Progress BarAttribute
### 制限
- int型
- long型
- double型
- float型

### 概要
- プログレスバーによる値の表示を行います
> 第一引数`min`: 横方向の拡大率  
> 第二引数`max`: 縦方向の拡大率  
> 第一引数`type`: プログレスバーを超過したときの処理の列挙型`ExcessType`  
>> 列挙型`ExcessType`の列挙子  
>> `None`: 処理しない  
>> `Clamp`: 範囲内に固定する  
>> `Around`: 超過分を周回させる  

### プレビュー
```C#
[ProgressBar(0f, 100f, ExcessType.Around)]
[SerializeField] float m_Progress;
```
[!] ここに **ProgressBarAttribute** の画像を設定

<br></br>

## ReadOnly Attribute
### 概要
- プロパティを編集不可にします

### プレビュー
```C#
[ReadOnly, SerializeField] int m_HashCode;
```
[!] ここに **ReadOnlyAttribute** の画像を設定

<br></br>

## ShowIf Attribute
### 概要
- プロパティの描画を条件化します
> 第一引数`condition`: 描画条件の文字列（結果がtrueのときに描画）
>> 対応演算子: `(` `)` `*` `/` `%` `+` `-` `==` `!=` `>=` `>` `<=` `<` `!` `&&` `||`

### プレビュー
```C#
public bool isShow;

[ShowIf("isShow")] public int indexA;
[ShowIf("isShow")] public int indexB;

[ShowIf("isShow && indexA + indexB > 0")] public Vector2Int position;
[ShowIf("isShow && position.x % 10 == 0")] public string tenText;
```
[!] ここに **ShowIfAttribute** の画像を設定

<br></br>

## Tag Attribute
### 制限
- int型
- string型

### 概要
- タグの種類から選んでタグ番号・タグ名を設定できるようにします

### プレビュー
```C#
[Tag] public int collisionTag;
```
[!] ここに **TagAttribute** の画像を設定

<br></br>

## Layer Attribute
### 制限
- int型
- string型

### 概要
- レイヤーの種類から選んでレイヤー番号・レイヤー名を設定できるようにします

### プレビュー
```C#
[Layer] public string[] itemLayer;
```
[!] ここに **LayerAttribute** の画像を設定