# Ceramic anchor contract utilities

![ceramicnetwork](https://circleci.com/gh/ceramicnetwork/js-ceramic.svg?style=shield)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![](https://img.shields.io/badge/Chat%20on-Discord-orange.svg?style=flat)](https://discord.gg/6VRZpGP)
[![Twitter](https://img.shields.io/twitter/follow/ceramicnetwork?label=Follow&style=social)](https://twitter.com/ceramicnetwork)

## Getting started

### Installation

```
$ npm install @ceramicnetwork/anchor-utils
```

### Usage

```ts
import {
  ANCHOR_CONTRACT_ADDRESSES,
  type SupportedNetwork,
} from "@ceramicnetwork/anchor-utils";

function getContractAddress(network: SupportedNetwork): string {
  const address = ANCHOR_CONTRACT_ADDRESSES[network];
  if (address == null) {
    throw new Error(`Unsupported contract network: ${network}`);
  }
}
```

## Development

Run tests:

```shell
npm test
```

Run linter:

```shell
npm run lint
```

## Contributing

We are happy to accept small and large contributions. Make sure to check out the
[Ceramic specifications](https://github.com/ceramicnetwork/ceramic/blob/main/SPECIFICATION.md)
for details of how the protocol works.

## License

MIT or Apache-2.0
