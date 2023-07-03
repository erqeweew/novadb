# Hyper Database

- Faster, Lightweight and Small advanced database.

## Installation

- We recommend to use [`pnpm`](https://npmjs.com/pnpm).

```bash
pnpm install hypr.db
```

## Features

- Faster
- Lightweight
- JSON, BSON and YAML databases
- TypeScript typing
- Written with ESM
- Small
- Over 20+ functions

## Usage

- We are supporting typing with [TypeScript](https://typescriptlang.org).

```ts
// ESM
import { Database } from 'hypr.db';

const db = new Database<{ 'hypr': string }>();

db.set('hypr', 'ok');
```

### Json Provider (Default)

```js
// ESM
import { Database } from 'hypr.db';

// CJS
const { Database } = require('hypr.db');

const db = new Database();

db.set('hypr', 'ok');
db.get('hypr');
db.exists('hypr');
db.del('hypr');
```

### Yaml Provider

- You need to download the [`yaml`](https://npmjs.com/yaml) module.

```bash
pnpm install yaml
```

```js
// ESM
import { Database, YAMLProvider } from 'hypr.db';

// CJS
const { Database , YAMLProvider } = require('hypr.db');
const provider = new YAMLProvider();
const db = new Database({ provider });

db.set('hypr', 'ok');
db.get('hypr');
db.exists('hypr');
db.del('hypr');
```

### Bson Provider

- You need to download the [`bson`](https://npmjs.com/bson) module.

```bash
pnpm install bson
```

```js
// ESM
import { Database, BSONProvider } from 'hypr.db';

// CJS
const { Database, BSONProvider } = require('hypr.db');
const provider = new BSONProvider();
const db = new Database({ provider });

db.set('hypr', 'ok');
db.get('hypr');
db.exists('hypr');
db.del('hypr');
```
