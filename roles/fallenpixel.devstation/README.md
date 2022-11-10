fallenpixel.devstation
=========

An ansible role to automate the installation of commonly used packages and
configuration used by fallenpixel.

Requirements
------------

Only ansible.builtin modules are used.

Role Variables
--------------

- dotfiles_repo: "fallenpixel/dotfiles"
  a dotfiles repository managed by GNU stow
- neovim_version: "0.6.1"
  The version of neovim installed IF the repository provided package is older than
  min_neovim_version
- min_neovim_version: "0.6.1"
  The minimum neovim version that is acceptable. A version older than min_neovim_version
  will be uninstalled and replaced with neovim's nightly appimage downloaded to
  /usr/local/bin

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: devstation
      roles:
         - { role: devstation, min_neovim_version: "0.6.1" }

License
-------

BSD

Author Information
------------------

fallenpixel/Eric Lehmann
https://katyl.info
