# 単語帳アプリ（AI駆動開発 実習）

輪講「AI駆動開発」の実習用リポジトリです。
AI のコーディングエージェント **Codex CLI** を使って、基本情報・応用情報の用語を4択で出題する単語帳アプリ（Python）を作ります。

| ファイル | 内容 |
| --- | --- |
| `requirements.md` | 要件定義書（課題1で Codex に渡す） |
| `words.csv` | 用語データ（30語） |
| `README.md` | この手順書 |

## 0. 必要なもの

| もの | 確認のしかた |
| --- | --- |
| Python 3.10 以上 | `python --version` |
| Git | `git --version` |
| ChatGPT アカウント | Plus・Pro・Business・Edu・Enterprise のプランで Codex を使えます（[詳しく](https://help.openai.com/en/articles/11369540-codex-in-chatgpt)） |

コマンドは、Windows では **PowerShell**、macOS / Linux では **ターミナル** で実行します。

## 1. リポジトリを取得する

```
git clone https://github.com/Eir-Vluv/wordbook.git
cd wordbook
```

> 「Code → Download ZIP」ではなく、必ず `git clone` で取得してください。
> Git の履歴があると、Codex の `/review` で変更点をレビューできます。

## 2. Codex CLI をインストールする

**Windows**（PowerShell）

```
powershell -ExecutionPolicy ByPass -c "irm https://chatgpt.com/codex/install.ps1 | iex"
```

**macOS / Linux**

```
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

npm や Homebrew を使っている人は、次の方法でも入れられます。

```
npm install -g @openai/codex
brew install --cask codex
```

インストールが終わったら、**ターミナルを開き直して**から次へ進みます。

## 3. 起動してサインインする

1. `wordbook` フォルダで Codex を起動します。
   ```
   cd wordbook
   codex
   ```
2. 初回は **Sign in with ChatGPT** を選び、ブラウザで ChatGPT にサインインします。
3. フォルダを信頼するか聞かれたら、許可します。

## 4. 動作を確認する

Codex の入力欄に次のように入力します。

```
このフォルダにあるファイルを教えて
```

`requirements.md` と `words.csv` が挙がれば準備完了です。`/quit` で終了します。

## 困ったとき

- `codex` が見つからない：ターミナルを開き直してから、もう一度 `codex` を実行してください。
- うまくいかない場合は、公式の手順も確認してください：[Codex CLI（OpenAI）](https://github.com/openai/codex)

---

ここから先の課題の進め方は、実習のスライドに沿って進めます。
