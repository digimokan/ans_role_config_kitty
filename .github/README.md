# ans_role_config_kitty

Install and configure the kitty terminal emulator.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_kitty.svg?label=release)](https://github.com/digimokan/ans_role_config_kitty/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install and configure the [kitty](https://sw.kovidgoyal.net/kitty/)
  terminal emulator.

## Supported Operating Systems

* Ubuntu focal (20.04), impish (21.10), jammy (22.04)
* Arch Linux
* FreeBSD

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_kitty
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the kitty terminal emulator"
         ansible.builtin.include_role:
           name: ans_role_config_kitty
           public: true
         vars:
           kitty_user_name: "user2"
   ```

## Role Options

See the role `defaults` files for main role vars listings:

  * [defaults](../defaults/main/)

Define these _required_ vars for the role:

  * `kitty_user_name`: user name of main kitty user

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_kitty/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

