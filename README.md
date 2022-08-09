# Sonarr role
This is a simple ansible role that installs sonarr.

## Configuration
As this role is pretty straight forward, it doesn't have that much configuration options.

### Defaults
Here's a list of default variables you may want to change.

| Name               | Default value | Description                                              |
|:-------------------|:--------------|:---------------------------------------------------------|
| sonarr_install_gpg | yes           | Specifies if this role should ensure that gpg is present |
| sonarr_version     | latest        | The version of sonarr to install                         |

### Vars
Here are some additional variables, that you probably don't want to overwrite.

| Name               | Default value                            | Description                                              |
|:-------------------|:-----------------------------------------|:-------------------------------|
| sonarr_key_server  | hkp://keyserver.ubuntu.com:80            | The key server used in apt_key |
| sonarr_key_id      | 2009837CBFFD68F45BC180471F4F90DE2A9B4BF8 | The id of the key              |