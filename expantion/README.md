
# エディタ拡張
エディタで編集する上での作業を楽にすることを目的としたエンジンの拡張クラスです

## ChangeActiveSelection.cs
### 概要
- カンマ(`,`)キーで選択しているオブジェクトのアクティブ/非アクティブを切り替えます 

<br></br>

## ComponentGUI.cs
### 概要
- ヒエラルキーウィンドウの各オブジェクトの右部にコンポーネントの一覧を表示するスクリプトです
- コンポーネントのアイコンは以下の定数から設定が変更できます
    - `icon_size`: 表示上のアイコンサイズ
    - `icon_transparency`: アイコンのアルファ値
    - `ignore_components`: 表示をしないコンポーネント  
	（`Transform`や`CanvasRenderer`など、表示されてなくとも支障のないコンポーネントに適用推奨）

### プレビュー
![ComponentGUI](https://github.com/Woskni/Woskni/assets/103394833/a580d69f-78d8-47b1-9c2b-b3145ed65883)
> コンポーネントをアイコン表示しているヒエラルキーウィンドウ

<br></br>

## DebugHotKey.cs
### 概要
- エディタ上で開発を行う際に活用できるショートカットキー用のスクリプトです
> `F1`キー: DebugHotKeyのヘルプをコンソールに出力  
> `F2`キー: Time.timeScale に 0.1 を減算（実行中のみ）  
> `F3`キー: Time.timeScale に 0.1 を加算（実行中のみ）  
> `F4`キー: Time.timeScale に 1.0 にリセット（実行中のみ）  
> `F5`キー: シーン再生・リロード（`ctrl + F5`: シーン停止, `shift + F5`: シーン一時停止）  
> `F6`キー: FPS（フレームレート）をコンソールに出力  
> `F7`キー: *未割当て*  
> `F8`キー: *未割当て*  
> `F9`キー: スクリーンショットを撮影  

<br></br>

## FileCountGUI.cs
### 概要
- プロジェクトウィンドウの各フォルダの最右やフォルダ内に、内蔵ファイルの個数を表示するスクリプトです

### プレビュー
![FileCountGUI](https://github.com/Woskni/Woskni/assets/103394833/f0b49307-65b7-46be-9cad-5e4ce6184d36)
> フォルダに内蔵ファイルの個数を表示しているプロジェクトウィンドウ

<br></br>

## Grouping.cs
### 概要
- 空のオブジェクトを生成して、選択したオブジェクトの親としてグループ化を行うスクリプトです

### プレビュー
![Grouping](https://github.com/Woskni/Woskni/assets/103394833/a5b7fb05-2fcc-41d1-8a4f-2a041f5af045)
> 選択オブジェクトのグルーピング処理を行う自作ウィンドウ

<br></br>

## HierarchyLines.cs
### 概要
- ヒエラルキーウインドウの各オブジェクトの親子関係・兄弟関係を罫線素片で明示化するスクリプトです

### プレビュー
![HierarchyLines](https://github.com/Woskni/Woskni/assets/103394833/efcf0901-f38b-40f7-bec0-8bb86ce9230f)
> 罫線素片によってオブジェクト同士の関係を示したヒエラルキーウィンドウ

<br></br>

## RenameSelection.cs
### 概要
- 選択したオブジェクトの名前を一括で変更・置換します

### プレビュー
![RenameSelection](https://github.com/Woskni/Woskni/assets/103394833/579a33c9-c942-43e8-b04f-52168949962e)
> 選択したオブジェクト名の置換処理を行う自作ウィンドウ

<br></br>

## RenderingMode.cs
### 概要
- マテリアルのブレンドモードに関係するスクリプトです
    - `GetAttachedBlend`関数: 引数マテリアルのブレンドモードを変更したマテリアルを返します
    - `CheckBlendMode`関数: 引数マテリアルがどのブレンドモードに該当するのかを列挙型`RenderingMode.Mode`で返します

<br></br>

## Screenshot.cs
### 概要
- ゲームウィンドウのスクリーンショットをPNG形式で保存します
- 保存した画像は`Assets/Screenshot(yyyy-MM-dd[HH-mm-ss)`で保存されます