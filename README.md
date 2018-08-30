# Deprecation

**This repo is deprecated**

We are deprecating and archiving
https://github.com/alphagov/datagovuk_infrastructure and since this repo is only
ever used from there, we are deprecating and archiving this as well.


# datagovuk_cf_scripts
Cloudfoundry Scripts for data.gov.uk

## ENV
* `CF_SECRETS_IDENTIFIER` - default 'secrets' - this value is whatever you call your credential-carrying user provided services

## Contents

* `set-credential <APP_NAME> <KEY> <VALUE>` - sets a single value on a user provided cf service
* `list-credentials <APP_NAME>` - spits out a JSON of secrets an app has access to
* `backup-credentials` - script that saves JSONs for all of the secrets repos
* `restore-credentials <PATH_TO_DUMP_JSON>` - takes a saved json from `backup-` or `list-credentials` and creates or updates the service
* `prune-old` & `prune-new` - easy delete for apps with `-old` or `-new` suffixes, e.g. from (old/failed) blue-green deploys
* `list-services` - dumps a JSON list of all your services, including credentials for any user provided services, and syslog drain url for any service with 'logit' in its name
* `syslog-drain` - prints the syslog drain url for a given app
