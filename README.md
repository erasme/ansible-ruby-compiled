ruby
====

This playbook will install a specific ruby version in a user's home directory.

Requirements
------------

None

Role Variables
--------------

  - `ruby_deploy_user`: taget user for rbenv installation; required; no
    default
  - `ruby_version`: Make options when building a ruby version;
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

