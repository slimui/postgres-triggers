# postgres-triggers
[![NPM](https://nodei.co/npm/postgres-triggers.png)](https://nodei.co/npm/postgres-triggers/)

Create trigger functions for changes (INSERT, UPDATE, DELETE) in tables.
The triggers will return a JSON object with some information and the changed row.

**This module is in its early stages. Feedback and PRs welcome!**
**Note**: io.js only for now!

## Install

```
npm i [-g] postgres-trigger
```

## Usage (CLI)

```
postgres-triggers postgres://foo@localhost:5432/db table1 table2 ...
```

## Usage (API)

```
const triggers = require('postgres-triggers')

triggers({ db: 'postgres://foo@localhost:5432/db', tables: [] }, function(err) {
  if (err) throw err
  console.log('done')
})
```

## TODO

- make it work with other types of ids (bigint only currently)
- make it work with differently named ids
- allow removal of triggers

## Tests

You need to give it a database connection string to be able to run the tests.
```
POSTGRES=postgres://postgres@localhost:5432/postgres npm test
```

## License
MIT
