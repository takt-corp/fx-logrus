# Logrus Logger for FX

fxlogrus provides a logger for [uber-go/fx](https://github.com/uber-go/fx) based on [sirupsen/logrus](https://github.com/sirupsen/logrus). All non-errors are logged as debug to keep the logs quiet, errors are still logged as errors.

```go

fx.New(
    // configure logger
    fx.WithLogger(func() fxevent.Logger {
        return &fxlogrus.LogrusLogger{Logger: logrus.StandardLogger()}
    }),
).Run()

```
