# kurt
```
kurt: KUbernetes Restart Tracker

A restart tracker that gives context to what is restarting in your cluster

Usage:
  kurt [command]

Available Commands:
  all         Print all groupings collected by kurt!
  completion  generate the autocompletion script for the specified shell
  help        Help about any command
  labels      Only print restart counts grouped by labels
  namespaces  Only print namespace-wide restart counts
  nodes       Only print node restart counts
  pods        Only print pod restart counts
  version     Print the current version and exit

Flags:
  -h, --help                help for kurt
  -l, --label strings       Specify multiple times for the label keys you want to see.
                            For example: "kurt all -l app"
  -c, --limit int           Limit the number of resources you want to see. Set limit to 0 for no limits. Must be positive.
                            For example: "kurt all -c=10" (default 5)
  -n, --namespace strings   Specify namespace for kurt to collect restart metrics.
                            Leave blank to collect in all namespaces.

Use "kurt [command] --help" for more information about a command.
```

# Requirements
Go Version 1.16

# Building
```
go build .
```
Outputs a `kurt` binary

# Testing
```
go test ./cmd -v
```
