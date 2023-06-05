# remark-stringify-nscode

**[remark](https://github.com/remarkjs/remark)** plugin to add support for serializing markdown into NSCode.

## Contents

- [remark-stringify-nscode](#remark-stringify-nscode)
  - [Contents](#contents)
  - [What is this?](#what-is-this)
  - [Install](#install)
  - [Use](#use)
  - [API](#api)
    - [`unified().use(remarkStringifyNSCode)`](#unifieduseremarkstringifynscode)
  - [Syntax](#syntax)
  - [Syntax tree](#syntax-tree)
  - [Types](#types)
  - [Contribute](#contribute)
  - [License](#license)

## What is this?

This package is a [unified](https://github.com/unifiedjs/unified) ([remark](https://github.com/remarkjs/remark)) plugin that defines how to take a syntax tree as input and turn it into serialized NSCode.

## Install

In Node.js:

```sh
npm install remark-stringify-nscode
```

In Deno:

```js
import remarkStringifyNSCode from "https://esm.sh/remark-stringify-nscode@latest";
```

In browsers:

```html
<script type="module">
  import remarkStringifyNSCode from "https://esm.sh/remark-stringify-nscode@latest?bundle";
</script>
```

## Use

```js
import { unified } from "unified";
import remarkParse from "remark-parse";
import remarkStringifyNSCode from "remark-stringify-nscode";

const file = unified()
  .use(remarkParse)
  .use(remarkStringifyNSCode)
  .processSync("**Hello, world!**");

console.log(String(file));

// Output:
// [b]Hello, world[/b]
```

## API

This package exports no identifiers.
The default export is `remarkStringifyNSCode`.

### `unified().use(remarkStringifyNSCode)`

Serializes markdown into NSCode.

## Syntax

At present, CommonMark syntax is supported with the exception of headings and inline code, which do not have a clear equivalent in NSCode.

## Syntax tree

The syntax tree format used in remark is [mdast](https://github.com/syntax-tree/mdast).

## Types

This package is fully typed with TypeScript.

## Contribute

Pull requests are welcome! Please also feel free to file an issue for [bug reports](https://github.com/esfalsa/remark-stringify-nscode/issues/new?assignees=&labels=bug&projects=&template=bug_report.yml) or [feature requests](https://github.com/esfalsa/remark-stringify-nscode/issues/new?assignees=&labels=enhancement&projects=&template=feature_request.yml).

## License

[MIT](./LICENSE) © [Pronoun](https://esfalsa.github.io)