# Ansible Collection - drew1kun.mac

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][collection-badge]][galaxy-link]

This collection contains Ansible roles for programmatic MacOS workstation configuration.
It is also a dependency for my workstation setup Ansible playbook.

The roles included:

  - `drew1kun.mac.mas` ([doc](https://github.com/drew1kun/ansible-collection-mac/blob/main/roles/mas/README.md))
  - `drew1kun.mac.macdock` ([doc](https://github.com/drew1kun/ansible-collection-mac/blob/main/roles/macdock/README.md))
  - `drew1kun.mac.macterm` ([doc](https://github.com/drew1kun/ansible-collection-mac/blob/main/roles/macterm/README.md))
  - `drew1kun.mac.pf` ([doc](https://github.com/drew1kun/ansible-collection-mac/blob/main/roles/pf/README.md))
  - `drew1kun.mac.refind` ([doc](https://github.com/drew1kun/ansible-collection-mac/blob/main/roles/refind/README.md))

## Installation

**NOTE:**
[drew1kun.fancyfonts][fancyfonts-collection-link] collection contains the dependency roles for `drew1kun.macterm` role.

Additionally **[optional]**, check out [drew1kun.slickshell][slickshell-collection-link]

[![FancyFonts Galaxy Role][fancyfonts-collection-badge]][fancyfonts-galaxy-link]
[![Slickshell Galaxy Role][slickshell-collection-badge]][slickshell-galaxy-link]

Install via Ansible Galaxy:

```
ansible-galaxy collection install \
	drew1kun.fancyfonts \
	drew1kun.mac
```

Alternatively, include this collection in your playbook's `requirements.yml` file:

```yaml
---
collections:
- name: drew1kun.fancyfonts
  version: '*'
  type: galaxy
- name: drew1kun.mac
  version: '*'
  type: galaxy
```
And run:

```
ansible-galaxy install -r requirements.yml
```

## Usage

Example of the play:

```yaml
- hosts: localhost
  connection: local
  collections:
  - drew1kun.mac
  roles:
    - mas
    - macdock
    - macterm
    - pf
```

## License

[MIT][mit-link]

## Author Information

Andrew Shagayev | [e-mail](mailto:drew-kun@protonmail.com)

[collection-badge]: https://img.shields.io/badge/collection-drew1kun.mac-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew1kun/mac
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-collection-mac/main/LICENSE

[fancyfonts-collection-badge]: https://img.shields.io/badge/collection-drew1kun.fancyfonts-green.svg
[fancyfonts-collection-link]: https://github.com/drew1kun/ansible-collection-fancyfonts
[fancyfonts-galaxy-link]: https://galaxy.ansible.com/drew1kun/fancyfonts

[slickshell-collection-badge]: https://img.shields.io/badge/collection-drew1kun.slickshell-green.svg
[slickshell-collection-link]: https://github.com/drew1kun/ansible-collection-slickshell
[slickshell-galaxy-link]: https://galaxy.ansible.com/drew1kun/slickshell
