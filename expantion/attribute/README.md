# 属性(Attribute)
インスペクタービューでのプロパティ表示に変化をもたらすクラスです

```C#
[Min(0)]
[System.Serializable]
[RequireComponent(typeof(SpriteRenderer))]
```
標準では以上のような属性が存在し、各括弧でくくりプロパティの宣言前に指定することで稼働します

<br></br>

## ChapterAttribute
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

## CommentAttribute
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

## FilePathAttribute
### 概要
- 
> 
> 