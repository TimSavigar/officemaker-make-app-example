# OfficeMaker Make App Example

Starter repository for a Make integration that calls the public OfficeMaker free API at `https://free.officemaker.ai`.

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

This repo is intended to prove the first Make story:

- take structured workflow data
- build `document_json`
- send it to OfficeMaker with snake_case POST fields
- return a downloadable Office file

## Next build steps

1. Turn the HTTP template into a polished Make app/module definition.
2. Add schema-aware payload builders for richer documents.
3. Add example scenarios for AI-generated letters and custom quotes.
