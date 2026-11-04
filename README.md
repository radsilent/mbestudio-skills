# Vector Stream Systems — Claude Code marketplace

Systems engineering skills for AI coding agents.

```
/plugin marketplace add radsilent/mbestudio-skills
```

## MBEstudio MCP server

Connect the AI tool you already use to MBEstudio: reverse engineer existing CAD
(STEP AP242, QIF), BOMs, KiCad netlists, ReqIF requirements and documents into one
traceable system model, then generate, verify, simulate and export it. Remote MCP
over Streamable HTTP; sign in with your email in the browser (OAuth 2.1, no API key).
Describing MBEstudio and estimating a job's cost need no account; paid tools show
the cost first and run only within the limit you set.

**Server URL:** `https://studio.vectorstreamsystems.com/mcp`

```bash
# Claude Code
claude mcp add --transport http --scope user mbestudio https://studio.vectorstreamsystems.com/mcp
# Codex
codex mcp add mbestudio --url https://studio.vectorstreamsystems.com/mcp && codex mcp login mbestudio
# VS Code (GitHub Copilot)
code --add-mcp '{"name":"mbestudio","type":"http","url":"https://studio.vectorstreamsystems.com/mcp"}'
```

Cursor, ChatGPT and Claude Desktop: add a remote MCP server (connector) with the URL above.
Setup for every client: https://vectorstreamsystems.com/agents ·
pricing: https://vectorstreamsystems.com/pricing · listed in the official MCP Registry.

### 日本語

既存の CAD（STEP AP242、QIF）、部品表、KiCad ネットリスト、ReqIF 要件、ドキュメントから、
トレーサブルな1つのシステムモデルを構築（リバースモデリング）し、お使いの AI ツール
（Claude Code、Codex、Cursor、ChatGPT、Claude Desktop、GitHub Copilot）から検証、
シミュレーション、エクスポートを実行できるリモート MCP サーバーです。派生開発（差分開発）で、
変更の影響範囲をモデル上で確認できます。

- サーバー URL: `https://studio.vectorstreamsystems.com/mcp`
- 設定手順（日本語）: https://vectorstreamsystems.com/ja/agents
- 料金（日本語）: https://vectorstreamsystems.com/ja/pricing

## Plugins

### `mbse-requirements` — free

Write, review and repair system requirements to aerospace and defence
standards. The five EARS patterns, permanent ID schemes, a banned-word list, and
a repair workflow that shows you the diff instead of silently rewriting your
spec.

```
/plugin install mbse-requirements@vector-stream-systems
```

[Details](plugins/mbse-requirements/README.md) ·
[MIT licence](LICENSE)

## The full pack

`mbse-requirements` is one skill of nine. The other eight cover safety analysis,
traceability, verification, a portable model format, and operating an MBEstudio
server. They are a one-time purchase:

**https://vectorstreamsystems.com/skillpack**

They are not in this repository and are licensed separately.

## Background reading

- [What is AI model-based systems engineering?](https://vectorstreamsystems.com/resources/what-is-ai-mbse):
  what AI can do in a SysML workflow today, where it fails, and how to check an
  AI-generated model before you rely on it.
- [AI SysML v2, from requirement to checked model](https://vectorstreamsystems.com/ai-sysml-v2):
  two plain-language requirements, the SysML v2 text written for them, and the
  compiler's value, limit and margin for each. The requirement shapes match the
  EARS patterns this plugin teaches.
- [SysML v2 tools compared](https://vectorstreamsystems.com/sysml-v2-tools):
  thirteen tools, where each runs and who it suits.

## Who makes this

[Vector Stream Systems LLC](https://vectorstreamsystems.com) —
streamline@vectorstreamsystems.com
