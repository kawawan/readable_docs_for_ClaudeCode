# readable_docs_for_ClaudeCode

Claude Codeが出力する情報密度の高い文章を、人間が読みやすい形にほぐすスキルです。

## こんな時に使えます
- Claude Codeの出力したドキュメントの情報密度が高くて読む気力が起きないとき
- 認知負荷が高いとき

## 使い方
明示的に呼び出したいときは `/読みやすい文章` コマンドを使用してください。単に「このドキュメントを読みやすくして」などでも発火すると思います。

## 導入方法
1. `readable-docs/` をダウンロード
2. `.claude/skills/` に配置

## 使用例：Before / After

**Before:**
> `atticbak/engine.py`。UIは無い。以下を直列で通す純粋関数の並び：
> `manifest.load` → `classify.assign_generation_tags`（GFS枠へ割当）→ `guard.exclude_guarded`（守護世代を除外）→ `select.pick_prune_candidates`（枠から溢れた世代を候補化）→ `plan.write_prune_plan`（`prune_plan.json` 出力）。**ここまでで削除は一切しない**。

**After:**
> 純粋関数を直列に並べます。前段から順に次のとおりです。
> 
> 1. manifest.load — マニフェストを読む。
> 2. classify.assign_generation_tags — GFS の枠へ世代を割り当てる。
> 3. guard.exclude_guarded — 守護世代を除外する。
> 4. select.pick_prune_candidates — 枠から溢れた世代を候補にする。
> 5. plan.write_prune_plan — prune_plan.json を出力する。
> 
> ここまでで削除は一切しません。

## 詳細
 → [ブログ記事(zenn)](https://zenn.dev/zekeynn/articles/4bbb34af17de57)
