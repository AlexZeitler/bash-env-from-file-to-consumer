# How to pass environment variables, defined in a file, to a consumer

Based on this [answer](https://stackoverflow.com/a/20909045/90800) at stackoverflow.

Running the sample:

```
env $(cat .env | xargs) ./consumer.sh
```

Expected output:

```
Hello, World!
```

If you call `env | grep "VAR1\|VAR2\|VAR3"`, output will be empty, thus the initial will not pass them to your environment permanently but to your `consumer.sh` only.
