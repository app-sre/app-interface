# App-Interface Example Data

This is example data for defining services based on [qontract-schema](https://github.com/app-sre/qontract-schemas).
This example data should be used to develop [qontract-reconcile](https://github.com/app-sre/qontract-reconcile).

## Setup

Parts of the [public repository](https://github.com/app-sre/app-interface) are objuscated, as some URLs and ids shouldn't be part of a public repo.
Fully usable data can be found [here](https://gitlab.cee.redhat.com/kfischer/app-interface-example-data).
That repo also contains automation to render the public repo.

### Current Issues

Some terraform resources are implemented with a single `.tfstate` file in mind.
This repository uses multiple `.tfstate` files on a single AWS account, which leads to issues during development.

While we are working on a fix, the current solution is:

1. Replace [those lines](https://github.com/app-sre/qontract-reconcile/blob/1bcdc21dd8a7719237e631b27a2f5f0752a95f3a/reconcile/utils/terrascript_client.py#L3462-L3465) with `es_deps = []`

## Context

For more context about this repo can be found [here](docs/background.md).
