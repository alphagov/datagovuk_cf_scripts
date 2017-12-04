# datagovuk_cf_scripts
Cloudfoundry Scripts for data.gov.uk

## Contents

* `set-credential <APP_NAME> <KEY> <VALUE>` - sets a single value on a user provided cf service
* `list-credentials <APP_NAME>` - spits out a JSON of secrets an app has access to
* `backup-credentials` - script that saves JSONs for all of the secrets repos
* `restore-service <PATH_TO_DUMP_JSON>` - takes a saved json from `backup-` or `list-credentials` and creates or updates the service
