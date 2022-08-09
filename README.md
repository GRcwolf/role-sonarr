# Sonarr role
This is a simple ansible role that installs sonarr on debian based systems.

## Compatibility
This role has only been tested on debian 11.
The role uses apt modules, so the role will only work on debian bases distributions.

## Configuration
As this role is pretty straight forward, it doesn't have that much configuration options.

### Defaults
Here's a list of default variables you may want to change.

| Name                        | Default value                        | Description                                              |
|:----------------------------|:-------------------------------------|:---------------------------------------------------------|
| sonarr_install_gpg          | yes                                  | Specifies if this role should ensure that gpg is present |
| sonarr_version              | latest                               | The version of sonarr to install                         |
| sonarr_distribution         | `{{ ansible_distribution }}`         | The distribution used for the apt repo                   |
| sonarr_distribution_release | `{{ ansible_distribution_release }}` | The distribution elease used for the apt repo            |

The variables `sonarr_distribution` and `sonarr_distribution_release` are used to add the apt repo.
Sonarr's repository may not support your specific distribution or release.
You can therefore use those varaibles to add the repo for a specific release or distribution, which is supported.

### Vars
Here are some additional variables, that you probably don't want to overwrite.

| Name               | Default value                            | Description                    |
|:-------------------|:-----------------------------------------|:-------------------------------|
| sonarr_key_server  | hkp://keyserver.ubuntu.com:80            | The key server used in apt_key |
| sonarr_key_id      | 2009837CBFFD68F45BC180471F4F90DE2A9B4BF8 | The id of the key              |