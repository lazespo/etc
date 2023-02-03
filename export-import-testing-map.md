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
bin/command export-import import --entity-type-list="ENTITY_TYPE1"
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
