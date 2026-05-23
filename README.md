# 🟢 LINEスタンプメーカー

ブラウザだけで動く、AI（OpenAI gpt-image-1）を使ったLINEスタンプ作成ツールです。
**サーバー不要・インストール不要・APIキーはあなたのブラウザにだけ保存**されます。

## ✨ できること

- テーマ・キャラクター設定を入力すると、人気LINEスタンプの定番セリフ（おはよう / ありがとう / おつかれ など）を自動で配分してくれる
- 8個 / 16個のスタンプセットを一括生成（背景透過PNG）
- 写真をアップロードして、その犬・猫・人物にそっくりなスタンプを作る
- 12種類のアートスタイル（線画 / 水彩 / アニメ / 3D / 写真リアル など）から選択
- スタンプごとに個別スタイル・追加指示・参考画像も指定可
- 履歴保存（IndexedDB）／ ZIP一括ダウンロード ／ フォルダ書き出し（Chrome/Edge）
- PC・スマホ両対応のレスポンシブUI

## 🚀 使い方

1. **OpenAI APIキー**を取得（[platform.openai.com](https://platform.openai.com/api-keys)）
   - `gpt-image-1` を使うため **Organization Verification（本人確認）が必須**
2. このサイトを開く
3. ⚙設定 ボタンから APIキーを貼り付け
4. テーマを入力 → セリフ案を作る → 一括で画像生成

### 料金の目安
- gpt-4o-mini（セリフ生成）: 1回 < $0.001
- gpt-image-1 medium 画質: 約 **$0.04 / 枚**
- 8枚セット = 約 **$0.32**

料金は全額あなたのOpenAIアカウントに請求されます。

## 🔒 プライバシー

- APIキーは**あなたのブラウザのlocalStorageにのみ保存**され、外部に送信されません
- このサイトの運営者・第三者はあなたのキーや生成画像にアクセスできません
- 生成された画像はOpenAIのサーバーを経由しますが、保管されません（OpenAI APIポリシー準拠）

## 🛠 技術構成

- 純粋なHTML/CSS/JavaScript（ビルド不要・依存ゼロ）
- 画像生成: OpenAI Images API (`gpt-image-1`)
- セリフ生成: OpenAI Chat API (`gpt-4o-mini`)
- 履歴保存: IndexedDB
- ZIP書き出し: JSZip（CDN）
- フォルダ書き出し: File System Access API（Chrome/Edge）

## 📝 ライセンス

MIT License — 自由に使用・改変・再配布できます（LICENSE参照）。

## ⚠ 注意事項

- OpenAIの利用規約・コンテンツポリシーに従って使用してください
- 実在キャラクター・芸能人・ブランドロゴの模倣はしないでください
- 生成物は[OpenAIのusage policies](https://openai.com/policies/usage-policies)に従う必要があります
- LINE Creators Marketへの申請には、画像の規格（370x320px等）への変換が別途必要です
