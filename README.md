# lenv

Support something like:

```shell
lenv tsx ./scripts/foo.ts
```

```json
{
  "scripts": {
    "joist-codegen": "lenv joist-codegen",
    "some-script": "lenv tsx ./scripts/foo.ts"
  }
}
```

Just import/require:

```
import "lenv";
```

Resolution:

* If `STAGE` is unset, set `STAGE=local`
* Load `env/${STAGE}.env`

What's different:

* Convention of `STAGE`
* Files are always in `env/`
* Files always end in `.env` so that IDEs know what they are
