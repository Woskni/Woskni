
## CSVLoader.cs
### 概要
- CSVファイルを外部から読み込む際に用いるクラスです

### 関数
- コンストラクタ: ファイルパスを指定してCSVファイルを読み込みます
- `GetString`関数: 引数 `row`, `col` から文字列を取得します
- `GetInteger`関数: 引数 `row`, `col` から整数を取得します
- `GetFloat`関数: 引数 `row`, `col` から実数を取得します
- `Find`関数: データの座標を検索し、Vector2Int型で返します

<br></br>

## EditorTheme.cs

### 列挙型
- `ThemeType`: ファイルパスの開始位置情報です
    > `Right`: ライトテーマ
    > `Dark`: ダークテーマ

### 概要
- Unityのエディタテーマ「ライトテーマ」「ダークテーマ」に関連する背景色・アイコン色の取得を行うクラスです

### 変数
- `lightThemeColor`: ライトテーマの背景色です
- `lightIconColor`: ライトテーマのアイコン色です
- `darkThemeColor`: ダークテーマの背景色です
- `darkIconColor`: ダークテーマのアイコン色です
- `theme`: エディタテーマの種類を列挙型`EditorTheme.ThemeType`で返します

### 関数
- `GetThemeColor`関数: 現在のテーマの背景色を返します
- `GetIconColor`関数: 現在のテーマのアイコン色を返します

<br></br>

## MeshCombiner.cs
### 概要
- メッシュの結合を行うクラスです

### 関数
- `Combine`関数
    - メッシュの結合を行います
        > 第一引数`gameObjects`: 結合するオブジェクト  
        > 第二引数`name`: 結合後のオブジェクトの名前  
        > 第三引数`parent`: 結合後のオブジェクトの親

<br></br>

## PathConverter.cs
### 概要
- ファイルパスを変換するクラスです

### 列挙型
- `FilePathType`: ファイルパスの開始位置情報です
    > `RootDirectoryPath`: ルートディレクトリからの絶対パス
    > `AssetsPath`: プロジェクトない
    > `CurrentDirectoryPath`: 

### 関数
- `Combine`関数
    - メッシュの結合を行います
        > 第一引数`gameObjects`: 結合するオブジェクト  
        > 第二引数`name`: 結合後のオブジェクトの名前  
        > 第三引数`parent`: 結合後のオブジェクトの親

