# VTuber Tipping Game V1

GitHub ActionsでAPKを作るための、Android WebView版ゲームプロジェクトです。  
`.github/workflows/build-apk.yml` が入っているので、GitHubにアップロードして `Run workflow` すればAPKを作れます。

## V1の内容

- 横画面固定
- タイトル画面
- 4人のキャラクター選択
- 配信画面
- 右側30%に投げ銭・稼ぐボタン
- 投げ銭累計で高額メニュー解放
- コメント欄・反応ログ
- タップで表情変更はなし

## GitHubでの使い方

1. このZIPを解凍する
2. 中身をGitHubのリポジトリにアップロードする
   - `.github` フォルダも必ずアップロード
3. GitHubの `Actions` タブを開く
4. `Build Android APK` を選ぶ
5. `Run workflow` を押す
6. 完了後、下の `Artifacts` から `vtuber-game-v1-debug-apk` をダウンロード
7. 中にある `app-debug.apk` をAndroid端末に入れてインストール

## 画像素材を差し替える場所

V1は仮素材なので、まずはCSSだけで動くようにしています。  
あとから画像を入れる場合は、主にこの3ファイルを編集します。

- `app/src/main/assets/index.html`
- `app/src/main/assets/styles.css`
- `app/src/main/assets/game.js`

## うまくいかない時

GitHub Actionsで失敗した場合は、失敗画面の赤いログ部分をスクショして見せてください。  
そのログに合わせて `build-apk.yml` かGradle設定を直せます。
