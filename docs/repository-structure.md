# リポジトリの構成と記録方針

## 置き場所の基準

| 内容 | 置き場所 | 例 |
|---|---|---|
| 端末・エディタ・Codex の再構築手順 | `setup/` | `macos.md`, `codex.md` |
| いつも守る判断基準 | `principles/` | `simplicity.md`, `verification.md` |
| 仕事の進め方 | `workflows/` | `bug-fix.md`, `code-review.md` |
| 一度限りでない調査結果 | `research/` | `2026-08-codex-context.md` |
| 変更しにくい方針の理由 | `decisions/` | `0001-agent-workflow.md` |
| この playbook 自体の案内 | `docs/` | `codex-engineering-playbook.md` |

## 記録するもの

次に当てはまるものは記録する。

- 三か月後の自分が判断理由を思い出せなさそうなこと
- 二回以上調べたこと、または再現した手順
- 失敗してから直した運用ルール
- 設定・依存関係・外部サービスの仕様に依存する手順

記録は短く始める。背景、結論、例外、確認日だけで十分なことが多い。

## 記録しないもの

- 特定プロジェクトだけにしか通用しない実装詳細
- その場の TODO や未検証の推測
- 公式ドキュメントを写しただけのメモ

プロジェクト固有の内容は、そのプロジェクトの README、設計文書、または ADR に置く。

## ADR の最小形式

重要な選択をしたら `decisions/NNNN-short-title.md` を作る。

```markdown
# ADR-0001: タイトル

## Status
Accepted

## Date
YYYY-MM-DD

## Context
何を決める必要があり、どんな制約があるか。

## Decision
何を採用するか。

## Alternatives considered
比較した案と採用しなかった理由。

## Consequences
得るもの、負うコスト、次に見直す条件。
```

古い ADR は削除しない。変更時は新しい ADR を作り、以前の記録を supersede する。
