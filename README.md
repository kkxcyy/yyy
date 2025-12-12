# yyy
yyy

## 回復摘要

- **回復提交 (Revert):** `6a2a9c0` — "Revert \"update layout\""。
- **被回復的提交:** `71da1a6` — "update layout"（修改了 `index.html`）。
- **簡要說明:** 先前的 `update layout` 提交造成 `index.html` 出現問題或回歸（參見前一個標記為 "Update index (contains bug)" 的提交 `27c07a7`），因此透過回復提交將該變更回退以還原穩定狀態。
- **後續操作建議:** 如需檢視差異或重新套用該變更，可使用 `git show 71da1a6`、`git show 6a2a9c0`，或在確認沒有衝突/問題後使用 `git cherry-pick 71da1a6` / `git revert 6a2a9c0`。
