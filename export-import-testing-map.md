# Export Import extension Testing Map

## Command examples

#### Export

```
bin/command export-import export --format=json --export-path="build/ExportImport/Export" --pretty-print
```

#### Import

```
bin/command export-import import --format=json --import-path="build/ExportImport/Import" --import-type=createAndUpdate --user-password="pass"
```

## Parameters testing

#### `--exportPath`

Define an export path.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --export-path="PATH"
```

Terminal result:

```
```

#### `--importPath`

Define an import path.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --import-path="PATH"
```

Terminal result:

```
```

#### `--entity-type-list`

The needed Entity type list can be defined. If empty, then gets all Entity types.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --entity-type-list="ENTITY_TYPE1"
```

Terminal result (export one entity):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --entity-type-list="ENTITY_TYPE1, ENTITY_TYPE2"
```

Terminal result (export several entities):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --entity-type-list="__APPEND__, ENTITY_TYPE1"
```

Terminal result (export - merge with a default list):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --entity-type-list="ENTITY_TYPE"
```

Terminal result (import one entity):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --entity-type-list="ENTITY_TYPE1, ENTITY_TYPE2"
```

Terminal result (import several entities):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --entity-type-list="__APPEND__, ENTITY_TYPE1"
```

Terminal result (import - merge with a default list):

```
```

#### `--importType`

The type of importing data.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --import-type=create
```

Terminal result (create):

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --import-type=createAndUpdate
```

Terminal result (create and update):

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --import-type=update
```

Terminal result (update):

```
```

#### `--pretty-print`

Store data in pretty print format.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --pretty-print
```

Terminal result:

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --pretty-print
```

Terminal result:

```
```

#### `--user-active`

Default user status for imported users. This applies to all user except admin user with ID `1`.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --user-active
```

Terminal result:

```
```

#### `--user-password`

User password for imported users. If empty then generates random values. For resetting the password use `bin/command set-password [username]`.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --user-password="PASSWORD"
```

Terminal result:

```
```

#### `--update-currency`

Update all currency fields. This option is depends on `currency`. If `currency` option is not defined, the default currency will be used instead.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --update-currency
```

Terminal result:

```
```

#### `--currency=""`

Currency symbol, ex. `USD`. If not defined, the default currency will be used instead.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --currency="UAH"
```

Terminal result:

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --currency="UAH"
```

Terminal result:

```
```

#### `--customization`

Export / import all customization made for the instance.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --customization

```

Terminal result:

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --customization

```

Terminal result:

```
```

#### `--config`

Export / import all customization made for the instance.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --config

```

Terminal result:

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --config

```

Terminal result:

```
```

#### `--update-created-at`

The current time will be defined for the `createdAt` field.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --update-created-at

```

Terminal result:

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --update-created-at

```

Terminal result:

```
```

#### `--hard-export-list`

This option enables export feature for an entity which is disabled in `exportImportDefs`.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --hard-export-list='ENTITY_TYPE'

```

Terminal result (for one entity):

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --hard-export-list='ENTITY_TYPE1, ENTITY_TYPE1'

```

Terminal result (for several entities):

```
```

#### `--hard-import-list`

This option enables import feature for an entity which is disabled in `exportImportDefs`.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --hard-import-list='ENTITY_TYPE'

```

Terminal result (for one entity):

```
```

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --hard-import-list='ENTITY_TYPE1, ENTITY_TYPE1'

```

Terminal result (for several entities):

```
```

#### `--config-ignore-list`

Additional ignore list for the config.

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --config-ignore-list="version"
```

Terminal result (export for version):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export --config-ignore-list="version, useCache"
```

Terminal result (export for version and useCache):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import export -config-ignore-list="__APPEND__, useCache"
```

Terminal result (export - merge with a default list):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --config-ignore-list="version"
```

Terminal result (import for version):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import --config-ignore-list="version, useCache"
```

Terminal result (import for version and useCache):

```
```

---

- [ ] SUCCESS
- [ ] FAILED

```
bin/command export-import import -config-ignore-list="__APPEND__, useCache"
```

Terminal result (import - merge with a default list):

```
``
