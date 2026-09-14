# tool-markdown-generator

Composable helpers for generating Markdown documents.

## Install

```sh
npm install @arylo-scripts/tool-markdown-generator
```

## Usage

```ts
import { MdTools, genTemplate, readTemplate } from '@arylo-scripts/tool-markdown-generator'

const markdown = genTemplate((utils) => {
  utils.h1('Title').listItem('First item').taskItem('Second item', { selected: true })
})

const nested = readTemplate(markdown, (utils) => {
  utils.h2('Links').hyperlink('Example', 'https://example.com')
})

const heading = MdTools.h1('Standalone heading')
```

Use `genTemplate` and `readTemplate` for fluent document construction, or
`MdTools` for individual Markdown primitives.

## API

- `genTemplate(callback?)`
- `readTemplate(text, callback?)`
- `MdTools`

## Development

```sh
npm install
npm test
npm run lint
npm run build
```
