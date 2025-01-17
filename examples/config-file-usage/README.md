# Example of using a config file

By using a config file `migrate.ts` or `migrate.json`, you can skip providing the options to the CLI command every time.

Fot demo purposes `migrate.ts` or `migrate.json` files were provided but you need you use only one

Now instead of running this command to create a new migration

Directory in this example is **not** the default `./migrations` but `./my-custom/migrations`.

```bash
npx migrate create my-new-migration -d mongodb://localhost/my-db
```

We can simply run

```bash
npx migrate create my-new-migration
```

You can change the name of the config file to expect by providing the `config` option e.g. `--config custom-config-file-name.json`
Note that this file has to be a valid `JSON` or `TypeScript` file with default export.

## Options override order

Note that options are overridden in the following order:

- Command line args > Env vars > Config file
