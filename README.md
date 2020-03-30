openprocurement.bridge.pricequotation
=====================================

Bot for Price Quotation procedure in eCatalogues which watching for tenders in `draft.publishing` and verify,
fill additional information from eCatalogues, such as:

```
- items[*].unit
- items[*].classification
- shortlistedFirms

```

And switch tender to `active.tendering` status and switch to `draft.invalid` if bot receive `HTTP 404` from eCatalogues or shortlistedFirms list will be empty.

## Development

```bash
$ git clone git@gitlab.qg:pricequotation/openprocurement.bridge.pricequotation.git
$ virtualenv -p python .venv
$ source .venv/bin/activate
$ pip install -r requirements-dev.txt
$ pip install -e .
```

## Run tests
```
$ pytest openprocurement/bridge/pricequotation/tests/ --cov=openprocurement/bridge/pricequotation
```

## How to use

```bash
$ databrige configuration.yaml
```