# My Notion Widgets

Notion埋め込み用のミニマルウィジェット集

## ウィジェット一覧

- **文字数カウンター** (`widgets/simple_character_counter.html`)  
  リアルタイム文字数カウント機能付きテキストエリア

## 使い方

1. GitHub Pages でホスティング
2. 各ウィジェットのURLをNotionに埋め込み

## ローカル開発

### 検証手順

1. ローカルサーバーを起動

   ```bash
   python3 -m http.server 8000
   ```

2. ブラウザでアクセス
   - メインページ: [http://localhost:8000](http://localhost:8000)
   - ウィジェット: [http://localhost:8000/widgets/](http://localhost:8000/widgets/)

3. 動作確認後、サーバーを停止

   ```bash
   # Ctrl+C でサーバーを停止
   ```
