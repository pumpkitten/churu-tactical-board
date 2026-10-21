# チュール式戦術ボード v0.77.3

キングダム覇道の作戦会議と進軍経路図を作る、単一 HTML の戦術ボードです。

## 公開アプリ

https://pumpkitten.github.io/churu-tactical-board/

## マップを直接開くリンク

| マップ | 施設数 | リンク |
| --- | ---: | --- |
| 従来25施設 | 25 | https://pumpkitten.github.io/churu-tactical-board/?map=original |
| 砦 | 18 | https://pumpkitten.github.io/churu-tactical-board/?map=fort |
| 山砦 | 16 | https://pumpkitten.github.io/churu-tactical-board/?map=mountain |
| 森砦 | 18 | https://pumpkitten.github.io/churu-tactical-board/?map=forest |
| 丘砦 | 16 | https://pumpkitten.github.io/churu-tactical-board/?map=hill |
| 城砦（旧） | 26 | https://pumpkitten.github.io/churu-tactical-board/?map=castle |
| 城砦（追加） | 26 | https://pumpkitten.github.io/churu-tactical-board/?map=castle-new |

URL に `?map=...` を付けると、指定したマップが最初から表示されます。
戦場選択欄の「🔗 マップURL」から、選択中のマップの URL をコピーすることもできます。

**安全対策:** ブラウザに別マップの自動保存がある場合は、既存の作戦を上書きしないよう確認します。
大切な作戦データは切り替え前に JSON 保存してください。

## v0.77 ～ v0.77.3 の主な変更点

- 従来25施設マップを含む7種類の戦場に対応。
- 山砦の進入禁止12区域、丘砦の進入禁止2区域を登録。経路チェックおよび迂回機能に対応。
- 城砦の17・18・23番は「兵器陣」。占拠から60秒経過すると井闌車が出現するゲームルールを記録（再生時の自動出現は未対応）。
- v0.77.1でマップごとの共有用URLに対応。
- **v0.77.3:** v0.77.2の城砦差し替えを取り消し、旧城砦を完全に復元。新画像は独立した7番目の「城砦（追加）」として登録しました。旧URL・旧施設番号を維持し、追加マップは `?map=castle-new` です。
- v0.76の通常作戦JSON読み込みを維持。

## 使い方

1. アプリ、または上記のマップ専用URLを開く。
2. 施設番号を確認し、駒や進軍ルートを作成する。
3. 「保存」で作戦JSONをダウンロードする。
4. JSON を開くときは「作戦JSONを開く」を使用する。

GitHub Pages公開アプリはブラウザ上で動作します。作戦はブラウザ内に自動保存されますが、別端末への引き継ぎには JSON 保存を使ってください。

## 互換性

作戦JSONの `format: "shirasu-tactical-board"` / `version: 12` は継続。これはアプリの見た目のバージョン番号とは別です。

## バックアップ

公開版の変更前ブランチ: `backup/pre-v0771-2026-10-21`。v0.77公開前: `backup/pre-v077-2026-10-21`。

## 共有プロジェクト利用者向け

v0.77.2で城砦の背景・施設位置が変わりました。ChatGPT共有プロジェクトに以前の6マップ登録データや城砦の空白JSONが登録されている場合は、最新版へ入れ替えてください。古い城砦作戦JSONは旧マップに合わせた位置を保持する可能性があるため、データを再利用する前に画面で経路を確認してください。
