# sqlboiler-crdb-fleetdb

## Original Source

This is a fork of the Metal Toolbox version of https://github.com/glerchundi/sqlboiler-crdb (found [here](https://github.com/infratographer/sqlboiler-crdb/v4)).

## Development/Modification
1. Clone this repository
2. Run a CRDB container on port 26257
3. Make your modifications.
4. Build and test as normal.
5. Push your branch, get reviewed, merge.
6. Update the client to use the new version.

## Installation

Installation is simple, just use go get. Once the binary (`sqlboiler-crdb-fleetdb`) is in your GOPATH sqlboiler will be able to use it if you run it with the driver name `crdb-fleetdb`.
```
# Install sqlboiler crdb driver
go get -u github.com/metal-toolbox/sqlboiler-crdb-fleetdb/v4
# Generate models
sqlboiler crdb-fleetdb
```
It's configuration keys in sqlboiler are simple:
```
[crdb-fleetdb]
user="root"
pass=""
host="localhost"
port=26257
dbname="mydatabase"
sslmode="disable"
```

(The following is from the original repo README)

**Notes**:
* I don't plan to support other than latest version of SQLBoiler.
Although, and in order to avoid confussion, major version appears in the import path.
* Cockroach 2.x and greater are supported, no plans to add support for previous versions.
* Code generation against secure clusters is not tested yet.
