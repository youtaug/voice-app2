# 会議議事録 自動作成ツール 🎙️

リアルタイム音声認識で会議の議事録を自動作成するWebアプリケーションです。

## 特徴

- 🎤 **リアルタイム音声認識**: ブラウザのWeb Speech APIを使用して、マイクからの音声をリアルタイムでテキスト化
- 📝 **2画面表示**: 認識されたテキストと編集可能な議事録を同時に表示
- 💾 **簡単ダウンロード**: ワンクリックでテキストファイルとして保存
- 🌐 **完全無料**: GitHub Pagesで静的サイトとしてホスト可能
- 🇯🇵 **日本語対応**: 日本語の音声認識に最適化

## 使い方

1. **会議情報の入力**
   - 会議タイトル、開催日、参加者を入力

2. **録音開始**
   - 「録音開始」ボタンをクリック
   - ブラウザからマイクの使用許可を求められたら「許可」をクリック

3. **音声認識**
   - 左側のエリアに認識されたテキストが自動で表示されます
   - 会議中、自動的に音声を認識し続けます

4. **議事録編集**
   - 右側のエリアで認識されたテキストを編集・整形
   - 左側のテキストをコピー＆ペーストして使用できます

5. **保存**
   - 「ダウンロード」ボタンで議事録をテキストファイルとして保存

## GitHub Pagesへのデプロイ方法

### 方法1: GitHubのWebインターフェースを使用（最も簡単）

1. GitHubで新しいリポジトリを作成
   - リポジトリ名: `meeting-minutes` （任意の名前でOK）
   - Public リポジトリとして作成

2. `meeting-minutes.html` をリポジトリにアップロード
   - 「Add file」→「Upload files」をクリック
   - `meeting-minutes.html` をドラッグ&ドロップ
   - 「Commit changes」をクリック

3. ファイル名を `index.html` に変更
   - `meeting-minutes.html` をクリック
   - 鉛筆アイコン（Edit）をクリック
   - ファイル名を `index.html` に変更
   - 「Commit changes」をクリック

4. GitHub Pagesを有効化
   - リポジトリの「Settings」タブをクリック
   - 左メニューから「Pages」をクリック
   - 「Source」で「Deploy from a branch」を選択
   - 「Branch」で `main` (または `master`) と `/root` を選択
   - 「Save」をクリック

5. 数分待つと、以下のURLでアクセス可能になります
   ```
   https://あなたのユーザー名.github.io/meeting-minutes/
   ```

### 方法2: Git コマンドラインを使用

```bash
# 新しいリポジトリを作成
mkdir meeting-minutes
cd meeting-minutes
git init

# HTMLファイルをindex.htmlとしてコピー
cp /path/to/meeting-minutes.html index.html

# コミットとプッシュ
git add index.html
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/あなたのユーザー名/meeting-minutes.git
git push -u origin main
```

その後、上記「方法1」の手順4でGitHub Pagesを有効化してください。

## 対応ブラウザ

- ✅ Google Chrome（推奨）
- ✅ Microsoft Edge
- ✅ Safari（iOS/macOSの最新版）
- ❌ Firefox（Web Speech API未対応）

## 使用上の注意

1. **マイクの許可が必要**: 初回使用時にブラウザからマイクの使用許可を求められます
2. **インターネット接続が必要**: 音声認識はクラウドベースで動作します
3. **静かな環境推奨**: 背景ノイズが少ない環境で使用すると認識精度が向上します
4. **長時間使用**: 連続で長時間使用する場合、時々録音を停止して再開すると安定します

## ショートカットキー

- `Ctrl + Shift + C`: 左側のテキストを右側にコピー

## カスタマイズ

HTMLファイルを直接編集することで、以下のカスタマイズが可能です：

- デザインの変更（CSSセクション）
- 会議情報のフィールド追加
- ダウンロードファイルのフォーマット変更

## トラブルシューティング

### 音声認識が動作しない
- ブラウザがマイクへのアクセスを許可しているか確認
- Chrome/Edge/Safariの最新版を使用しているか確認
- HTTPSまたはlocalhostで動作しているか確認（HTTPでは動作しません）

### 認識精度が低い
- マイクに近づいて話す
- 背景ノイズを減らす
- ゆっくりはっきり話す

## ライセンス

MIT License - 自由に使用・改変・配布可能です

## 開発者

Made with ❤️ for TKP Meeting Minutes
