# OpenFinance Mintlify Docs

Documentation site for OpenFinance MCP, built with [Mintlify](https://mintlify.com).

## Local preview

Install the Mintlify CLI:

```bash
npm i -g mint
```

Run the dev server from the docs root:

```bash
mint dev
```

Visit `http://localhost:3000` to preview.

## Deploy

1. Sign up at [mintlify.com](https://mintlify.com) and create a new project.
2. Connect this repo (GitHub, GitLab, or Bitbucket).
3. Point Mintlify at the docs folder. It will read `docs.json` automatically.
4. Every push to `main` triggers a redeploy.

## Structure

```
.
├── docs.json                 ← Navigation and theme config
├── introduction.mdx          ← Landing page
├── getting-started/
│   ├── quick-install.mdx
│   ├── skills-vs-mcp.mdx
│   ├── api-keys.mdx
│   └── installing-skills.mdx
├── installation/
│   ├── coding-agents/
│   │   ├── claude-code.mdx
│   │   ├── codex.mdx
│   │   ├── cursor.mdx
│   │   ├── vscode.mdx
│   │   ├── windsurf.mdx
│   │   ├── cline.mdx
│   │   ├── openclaw.mdx
│   │   └── hermes.mdx
│   └── chat-clients/
│       ├── claude-desktop-macos.mdx
│       ├── claude-desktop-windows.mdx
│       ├── claude-ai-web.mdx
│       ├── chatgpt.mdx
│       └── manus.mdx
└── reference/
    ├── verifying-connection.mdx
    └── troubleshooting.mdx
```

## Editing

All pages are MDX, frontmatter at the top sets the title and description. Mintlify components used:

- `<Steps>` / `<Step>` for sequential instructions
- `<Tabs>` / `<Tab>` for variant configurations (public vs wallet)
- `<CardGroup>` / `<Card>` for navigation tiles
- `<Note>`, `<Warning>`, `<Tip>` for callouts
- `<AccordionGroup>` / `<Accordion>` for collapsible sections

Full component reference: [mintlify.com/docs](https://mintlify.com/docs).
