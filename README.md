# OfficeMaker + Make — AI document workflow automation example

This repository demonstrates a **Make** scenario calling **OfficeMaker** to create native Word (`.docx`), Excel (`.xlsx`) and PowerPoint (`.pptx`) files from structured workflow data.

Use Make for visual orchestration and branching. Use OfficeMaker when the workflow reaches the document-execution step.

**Make scenario → filter/transform data → structured JSON → OfficeMaker → native Office file**

## Canonical OfficeMaker resources

- [OfficeMaker](https://officemaker.ai/)
- [AI workflow automation tools](https://officemaker.ai/ai-workflow-automation-tools)
- [Document generation API](https://officemaker.ai/document-generation-api)

- [OfficeMaker evidence hub](https://officemaker.ai/evidence)
- [Token-efficiency methodology](https://officemaker.ai/evidence/token-efficiency-methodology)
- [MCP document generation](https://officemaker.ai/mcp-document-generation)
- [AI document workflow automation tools](https://officemaker.ai/blog/best-ai-document-workflow-automation-tools)

## What is included

- a lightweight OfficeMaker client in `src/officemaker-client.mjs`
- sample document builders for Word, Excel, and PowerPoint
- runnable local scripts in `scripts/`
- a Make HTTP module starter payload in `make/http/create-document-request.json`

## Quick start

```bash
npm run create:letter
npm run create:quote
npm run create:deck
```

## Platform fit

This repository demonstrates the first Make workflow pattern:

1. collect or transform structured workflow data;
2. build the OfficeMaker `document_json`;
3. send it to OfficeMaker;
4. receive a native Office artifact;
5. continue the Make scenario with storage, approval or notification.

## Why the separation matters

The language model does not need to manipulate low-level Office file structures. OfficeMaker works from schema-led JSON and performs document construction in middleware. This can reduce unnecessary model context and code-generation loops in suitable workflows.

## Important status

This repository is an **integration example**, not a claim of an official Make App Marketplace listing. It uses Make's generic HTTP integration pattern.

## Next build steps

1. Turn the HTTP template into a polished Make app/module definition.
2. Add schema-aware payload builders.
3. Add example scenarios for AI-generated letters, reports and proposal packs.
4. Pursue marketplace publication only after the module is production-ready.
