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

## 詳細歷程（最近 12 次提交）

以下列出最近 12 次提交的摘要（SHA、作者、日期、標題、變更檔案與備註）：

- `f9a7251` — unknown — 2025-12-12 23:45:02 +0800 — docs: add commit history and PR flow demo section — README.md
	- 備註：新增「Commit 歷程及 PR 流程示範」並記錄示範流程。
	- 連結：https://github.com/kkxcyy/yyy/commit/f9a7251

- `27dd622` — unknown — 2025-12-12 23:42:50 +0800 — revert: revert demo merge to show revert flow — README.md
	- 備註：撤銷先前合併提交（08516a6），示範如何在 main 上撤銷 merge。
	- 連結：https://github.com/kkxcyy/yyy/commit/27dd622

- `08516a6` — unknown — 2025-12-12 23:37:30 +0800 — chore: resolve merge conflict and merge feature/demo-revert into main
	- 備註：合併 demo 分支 `feature/demo-revert` 到 `main`，解決 README.md 的合併衝突後完成合併。
	- 連結：https://github.com/kkxcyy/yyy/commit/08516a6

- `d909458` — unknown — 2025-12-12 23:31:54 +0800 — docs: demo commit for merge and revert flow — README.md
	- 備註：示範性的 commit，為操練 merge/revert 流程建立內容。
	- 連結：https://github.com/kkxcyy/yyy/commit/d909458

- `bd31e44` — kkxcyy — 2025-12-12 23:31:28 +0800 — Update README.md — README.md
	- 備註：先前對 README 的更新。
	- 連結：https://github.com/kkxcyy/yyy/commit/bd31e44

- `fd5055a` — unknown — 2025-12-12 23:29:33 +0800 — docs: add revert summary to README — README.md
	- 備註：加入 revert 摘要（回復哪個提交），整理回復原因的簡述。
	- 連結：https://github.com/kkxcyy/yyy/commit/fd5055a

- `d77de94` — kkxcyy — 2025-12-08 22:48:21 +0800 — Merge pull request #2 from kkxcyy/feature/skills-bars
	- 備註：合併 `feature/skills-bars` 到 `main`。
	- 連結：https://github.com/kkxcyy/yyy/commit/d77de94

- `3f2acb9` — unknown — 2025-12-08 22:37:37 +0800 — skills switch to bar ver — index.html
	- 備註：技能展示切換為進度條版本（後來又有標籤雲的變更）。
	- 連結：https://github.com/kkxcyy/yyy/commit/3f2acb9

- `18b4395` — unknown — 2025-12-08 11:46:41 +0800 — update layout, add skills — index.html
	- 備註：更新 layout 並新增技能展示的初始版本。
	- 連結：https://github.com/kkxcyy/yyy/commit/18b4395

- `6a2a9c0` — unknown — 2025-12-08 11:37:49 +0800 — Revert "update layout" — index.html
	- 備註：還原 `update layout` 的變更，回復 `index.html` 的先前內容。
	- 連結：https://github.com/kkxcyy/yyy/commit/6a2a9c0

- `27c07a7` — unknown — 2025-12-08 11:36:50 +0800 — Update index (contains bug) — index.html
	- 備註：更新 `index.html`，該提交被標示包含 bug，之後被回復或修正。
	- 連結：https://github.com/kkxcyy/yyy/commit/27c07a7

- `71da1a6` — unknown — 2025-12-08 11:32:02 +0800 — update layout — index.html
	- 備註：layout 更新提交（之後被回復）。
	- 連結：https://github.com/kkxcyy/yyy/commit/71da1a6

---

### 詳細版本歷史（含變更檔案與檢視指令）

為便於追蹤，每筆提交都包含變更檔案的清單與查看 diff 的指令範例：

1. `ec1dd85` — unknown — 2025-12-12 23:52:56 +0800 — docs: add detailed recent commit history to README
	- Files changed: README.md
	- Note：新增「詳細歷程」，補充更多版本歷史資訊。
	- View diff：`git show ec1dd85`

2. `f9a7251` — unknown — 2025-12-12 23:45:02 +0800 — docs: add commit history and PR flow demo section
	- Files changed: README.md
	- Note：新增 commit 歷程示範段落與 PR 流程說明。
	- View diff：`git show f9a7251`

3. `27dd622` — unknown — 2025-12-12 23:42:50 +0800 — revert: revert demo merge to show revert flow
	- Files changed: README.md
	- Note：撤銷先前示範合併的變更，以示範 revert 操作。
	- View diff：`git show 27dd622`

4. `08516a6` — unknown — 2025-12-12 23:37:30 +0800 — chore: resolve merge conflict and merge feature/demo-revert into main
	- Files changed: README.md
	- Note：合併 `feature/demo-revert` 到 `main`，並在合併時解決 README.md 的衝突。
	- View diff：`git show 08516a6`

5. `d909458` — unknown — 2025-12-12 23:31:54 +0800 — docs: demo commit for merge and revert flow
	- Files changed: README.md
	- Note：示範性的 commit (Feature branch: `feature/demo-revert`)。
	- View diff：`git show d909458`

6. `bd31e44` — kkxcyy — 2025-12-12 23:31:28 +0800 — Update README.md
	- Files changed: README.md
	- Note：先前對 README 的更新。
	- View diff：`git show bd31e44`

7. `fd5055a` — unknown — 2025-12-12 23:29:33 +0800 — docs: add revert summary to README
	- Files changed: README.md
	- Note：加入 revert 摘要（回復哪個提交），整理回復原因。
	- View diff：`git show fd5055a`

8. `d77de94` — kkxcyy — 2025-12-08 22:48:21 +0800 — Merge pull request #2 from kkxcyy/feature/skills-bars
	- Files changed: (merge commit)
	- Note：合併 feature/skills-bars 到 main，包含技能顯示樣式調整。
	- View diff：`git show d77de94`

9. `3f2acb9` — unknown — 2025-12-08 22:37:37 +0800 — skills switch to bar ver
	- Files changed: index.html
	- Note：將技能展示切換為進度條版本。
	- View diff：`git show 3f2acb9`

10. `18b4395` — unknown — 2025-12-08 11:46:41 +0800 — update layout, add skills
	 - Files changed: index.html
	 - Note：主要更新網頁 layout 與新增技能展示區塊。
	 - View diff：`git show 18b4395`

11. `6a2a9c0` — unknown — 2025-12-08 11:37:49 +0800 — Revert "update layout"
	 - Files changed: index.html
	 - Note：撤銷先前的 layout 更新（update layout）。
	 - View diff：`git show 6a2a9c0`

12. `27c07a7` — unknown — 2025-12-08 11:36:50 +0800 — Update index (contains bug)
	 - Files changed: index.html
	 - Note：更新 index，之後被回復或修正（標註含 bug）。
	 - View diff：`git show 27c07a7`



