# foreman-automation-tools
Manage updates of content views in Foreman/Katello.

## update-content-views
```
usage: update-content-views [-h] [--dry-run] [--verbose]
                            [--description STRING] [--composite-view NAME]
                            {update,promote} ...

Manage updates of content views in Foreman/Katello.

positional arguments:
  {update,promote}      sub-command help
    update              update content views
    promote             promote content view versions

optional arguments:
  -h, --help            show this help message and exit
  --description STRING  set comment added to update operations
  --composite-view NAME
                        only update/promote this composite view (multiple
                        allowed)
  --dry-run             stop before any action which changes existing data
  --verbose, -v         give more information during operations

Typical usage:

  First use 'hammer auth login' to authenticate.

  To update the staging environment:
    update-content-views -v update --promote-to Staging

  To promote previously staged changes to the production environment:
    update-content-views -v promote --from Staging --to Production

  To delete the oldest content views:
    update-content-views -v expire
```
