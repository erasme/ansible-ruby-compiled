ruby
====

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-ruby.svg?style=flat)](http://travis-ci.org/erasme/ansible-ruby)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansibe-ruby-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-ruby/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.ruby-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2910)

This playbook will install a specific ruby version in a user's home directory.

Requirements
------------

None

Role Variables
--------------

  - `ruby_version`: Ruby version to install
  - `ruby_deploy_user`: target user for rbenv installation; required; no
    default
  - `ruby_makeopts`: Make options when building a ruby version;
    optional; default: -j2
  - `ruby_default`: default ruby version to set

Tags
----

  - `ruby` : applies to th whole role
  - `ruby:config` : applies to the configuration part only
  - `ruby:install` : applies to the ruby compilation/installation part only

Dependencies
------------

  - erasme.rbenv

Example Playbook
----------------

This is mainly used as a dependency in your existing playbooks, like:

    dependencies:
      - { role: ruby,
          version: "2.2.0",
          ruby_default: "2.2.0" }

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

