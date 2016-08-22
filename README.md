# cli-snippets
Useful shell script snippets for embedding elsewhere...

### logging

`logger.sh` provides simple logging functions, with optional supression of `INFO` and `DEBUG`. For example, the following script:
```
#!/bin/bash
source logger.sh
unset LOG_INFO
log_warn 'look out!'
log_error ouch... not good
log_info some info
log_debug some debug statement
```

Produces the following output:
```
2016-08-22T22:15:49Z example.sh[91161] WARN: look out!
2016-08-22T22:15:49Z example.sh[91161] ERROR: ouch... not good
2016-08-22T22:15:49Z example.sh[91161] DEBUG: some debug statement
```
