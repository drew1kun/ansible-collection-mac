# Ansible role: mas

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Ansible role for installing the apps from MacOS App Store.

This role is a fork of geerlingguy.mas role, which does not work for me for some reason.

Requirements
----

MacOS on the configured host.

Role Variables
----

| Variable | Description | Default |
|----------|-------------|---------|
| `mas_email` | Email registered for AppStore purchases | `<empty>` |
| `mas_password` | Password used buy mas for AppStore purchases | `<empty>` |
| `mas_installed_apps[]` | List of apps to be installed | see [`defaults/main.yml`](defaults/main.yml) |
| `mas_upgrade_all_apps` | Upgrade installed apps? | `no` |
| `mas_signin_dialog` | Show sign in dialog? | `no` |
| `mas_software_update.install` | Determine if softwareupdate should install or just download updates | `false` |
| `mas_software_update.recommended` | Determine if softwareupdate should install all or recommended updates only | `false` |

Dependencies
----

None.

Example Playbook
----

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: dev_clients
  roles:
  - role: drew1kun.mas
```

License
----

[MIT][mit-link]

Author Information
----

Andrew Shagayev | [e-mail](mailto:drewshg@gmail.com)

[role-badge]: https://img.shields.io/badge/role-drew1kun.mas-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew1kun/mas/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-mas/master/LICENSE
