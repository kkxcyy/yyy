# yyy
yyy

## 回復摘要

- **回復提交 (Revert):** `6a2a9c0` — "Revert \"update layout\""。
- **被回復的提交:** `71da1a6` — "update layout"（修改了 `index.html`）。
- **簡要說明:** 先前的 `update layout` 提交造成 `index.html` 出現問題或回歸（參見前一個標記為 "Update index (contains bug)" 的提交 `27c07a7`），因此透過回復提交將該變更回退以還原穩定狀態。
- **後續操作建議:** 如需檢視差異或重新套用該變更，可使用 `git show 71da1a6`、`git show 6a2a9c0`，或在確認沒有衝突/問題後使用 `git cherry-pick 71da1a6` / `git revert 6a2a9c0`。
 
## Commit 歷程及 PR 流程示範

以下是演示流程中發生的提交與分支操作，包含一次 merge 與之後的 revert（撤銷）操作：

- 建立分支並提交（feature branch）：
	- 分支：`feature/demo-revert`
	- 提交（commit）：`d909458` — `docs: demo commit for merge and revert flow`

- 合併（merge）分支到 `main`：
	- 合併提交（merge commit）：`08516a6` — `chore: resolve merge conflict and merge feature/demo-revert into main`
	- 若你在 GitHub 上建立 PR 並合併，PR 連結（示例）：
		- https://github.com/kkxcyy/yyy/pull/new/feature/demo-revert

- 撤銷（revert）合併提交：
	- Revert 提交：`27dd622` — `revert: revert demo merge to show revert flow`
	- 指令範例：
		```powershell
		git revert -m 1 08516a6
		git commit -m "revert: revert demo merge to show revert flow"
		git push origin main
		```

流程簡述：建立 feature 分支 -> 提交變更 -> 在 GitHub 開 PR 並合併到 main -> 若合併有問題，使用 `git revert -m 1 <merge-commit>` 來撤銷合併（會在 main 上再產生一個 revert 提交）。

