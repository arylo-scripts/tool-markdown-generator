# tool-markdown-generator

Composable helpers for generating Markdown documents.

## Install

```sh
npm install github:arylo-scripts/tool-markdown-generator
```

## Usage

```ts
import { genTemplate } from '@arylo-scripts/tool-markdown-generator'

const markdown = genTemplate((utils) => {
  utils.h1('Title')
  utils.listItem('First item')
  utils.listItem('Second item')
})
```

## Development

```sh
npm install
npm test
npm run lint
npm run build
```
