# 定跡まとめ（shogi-joseki）

個人の将棋定跡（棋譜 `.kifu` と要点メモ `定跡まとめ.md`）を整理・履歴管理するリポジトリです。GitHub で履歴管理し、ローカルから DropBox に自動バックアップできます。

## 目的
- 定跡・研究棋譜の一元管理
- Git による差分と履歴の確認
- DropBox へのバックアップ（GitHub Actionsで自動実行）
- スマフォアプリからDropBoxのファイルを参照する

## リポジトリ構成
- 各戦法フォルダ（例: 3間飛車-居飛車, 中飛車, 相振り3間飛車）
  - 棋譜: `.kifu` ファイル
  - メモ: `定跡まとめ.md`
- スクリプト: sync_to_dropbox.py（Git 差分を DropBox にアップロード）

## 必要環境
- Python 3.8+
- `dropbox` パッケージ

インストール例:
```bash
python -m pip install --upgrade pip
python -m pip install dropbox
```

## 注意事項
- DropBox 認証情報を公開リポジトリへ置かないでください。
- 大きなファイルはネットワークや API 制限に注意してください。
- `.kifu` の閲覧には外部の kifu ビューアをお使いください。