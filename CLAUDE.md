# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

汎用AIスキル集リポジトリ。LLMやAIエージェントが活用できるスキル定義（SKILL.md）のコレクション。Claude Codeに限らず、様々なAIツールやエージェントで利用可能な、言語非依存のワークフロー・方法論を定義する。

## リポジトリ構造

```
skills/
└── skills/
    └── <skill-name>/
        └── SKILL.md
```

各スキルは `skills/` 配下に独自のディレクトリを持ち、`SKILL.md` ファイルで定義される。

## SKILL.md のフォーマット

YAML frontmatter が必須：
- `name`: スキル識別子（kebab-case、ディレクトリ名と一致）
- `description`: スキルの説明とトリガー条件（いつ発動すべきか）

本文にはワークフロー定義をmarkdownで記述する（手順、ルール、例、判断基準など）。

## スキルの追加方法

1. `skills/<skill-name>/` ディレクトリを作成
2. frontmatter（`name`, `description`）付きの `SKILL.md` を配置
3. 1スキル = 1つの方法論・ワークフローに集中させる
4. `description` にはトリガー条件を明確に記述する

## 規約

- スキル名は kebab-case
- スキル内容は日本語で記述
- 各スキルは自己完結させる（スキル間の相互参照はしない）
- ビルド・テスト・CIなし（純粋なドキュメントリポジトリ）
