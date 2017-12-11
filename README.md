# foreman-automation-tools
Manage updates of content views in Foreman/Katello.

## update-content-views
```
usage: update-content-views [-h] --account-info JSONFILE
                            [--description STRING] [--composite-view NAME]
                            [--dry-run] [--verbose]
                            {update,promote} ...

Manage updates of content views in Foreman/Katello.

positional arguments:
  {update,promote}      sub-command help
    update              update content views
    promote             promote content view versions

optional arguments:
  -h, --help            show this help message and exit
  --account-info JSONFILE
                        contains username and password
  --description STRING  set comment added to update operations
  --composite-view NAME
                        only update/promote this composite view (multiple
                        allowed)
  --dry-run             stop before any action which changes existing data
  --verbose, -v         give more information during operations

Typical usage:

  To update the staging environment:
    update-content-views --account-info /path/to/accountinfo.json -v update --promote-to Staging

  To promote previously staged changes to the production environment:
    update-content-views --account-info /path/to/accountinfo.json -v promote --from Staging --to Production
```
