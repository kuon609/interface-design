# interface-design

Webアプリケーション（SaaS・管理画面・ダッシュボード）向けの UI/UX ベストプラクティスと
アンチパターンを詰め込んだ Claude Code Plugin。

## 内容

### Skill: `ui-best-practices`

UI を実装するときに常時参照されるガイド。以下をカバーする：

- **スペーシングシステム** — Base-8 スケールの徹底、任意の値の禁止
- **視覚的階層** — 3 レベルルール、プライマリアクションの明確化
- **コンポーネント状態** — ホバー・フォーカス・ローディング・空・エラーの完全実装
- **カラーセマンティクス** — セマンティックロールの定義と一貫した使用
- **フォーム UX** — ラベル、バリデーションタイミング、エラー回復
- **アンチパターンチェックリスト** — リリース前に確認すべき項目

### Command: `/ui-review`

既存コードの UX・デザインパターンを明示的にレビューする（RAMS のデザインパターン版）。

```bash
/ui-review src/components/UserForm.tsx
```

RAMS（アクセシビリティ）と組み合わせて使うことで、アクセシビリティと UX の両方をカバーできる。

## 参照ファイル

| ファイル | 内容 |
|---------|------|
| `skills/ui-best-practices/references/visual-design.md` | スペーシング・カラー・タイポグラフィ・レイアウト |
| `skills/ui-best-practices/references/states.md` | ローディング・空・エラー・フィードバックパターン |
| `skills/ui-best-practices/references/ux-patterns.md` | アフォーダンス・フォーム・ナビゲーション・モーダル |
| `skills/ui-best-practices/references/antipatterns.md` | ダークパターン・UX ミス・視覚的混乱・コードレベルの問題 |

## インストール

### Marketplace から

```bash
/plugin marketplace add kuon609/interface-design
/plugin install interface-design
```

### 直接インストール

```bash
/plugin install github:kuon609/interface-design
```

## 他のプラグインとの関係

| プラグイン | 役割 | 本プラグインとの違い |
|-----------|------|------------------|
| **RAMS** | アクセシビリティ（WCAG）レビュー | RAMS は aria/a11y 専門、本プラグインは UX パターン専門 |
| **frontend-design** | 美的デザイン・クリエイティブ生成 | frontend-design は創造性、本プラグインは一貫性・パターン |

3 つ組み合わせることで、アクセシビリティ・UX・美的デザインをすべてカバーできる。

## ライセンス

MIT
