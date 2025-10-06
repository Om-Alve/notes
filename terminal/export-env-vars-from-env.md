#terminal #bash 
## Managing Environment Variables in Bash

### What Happens with `source .env`

`source .env` loads variables as **shell-only variables** i.e. they won't be exported to subprocesses.

### To export variables in an env file so that subprocesses can access them, you can:

```bash
set -a # Automatically export all env vars defined after this
source .env
set +a # Stop exporting env vars now.
```

> BTW -> `source` is synonymous to `.`
