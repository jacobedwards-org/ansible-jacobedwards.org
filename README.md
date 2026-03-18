Ansible Roles & Playbooks for jacobedwards.org
==============================================

These roles and playbooks will eventually have full coverage of all
the services on jacobedwards.org. Since this is my first real Ansible
project, expect a lot of breaking changes as I learn best practices.

Objectives
----------

One major reason for formalizing this system in Ansible is
self-documentation and version control. Aside from that, there are
these main objectives:

- Full configuration & maintenance coverage for jacobedwards.org.
- Full outcome and variable documentation for roles.
- Generic, reusable roles.

Playbooks
---------

Playbooks are located under the `playbooks` directory. The following
playbooks are available:

- `site.yml` — Main playbook to fully configure the system.
- `update.yml` — Update packages and apply system patches.
- `upgrade.yml` — Upgrade the system to the next OpenBSD release.

Additionally, the `bin/runrole` script is included to generate and
execute a temporary playbook for the roles specified as arguments.

Ansible Vault
-------------

Ansible's `vault_password_file` is set to `bin/vault-password` which
is a script that uses an internal password managing utility to
supply the password. It will need to be modified before use.

Tags
----

- `init` — These tasks only need to be run once and initialize the role.
- `config` — These tasks are run to update configurations for a role.
- `runtime` — These tasks can be initiated for runtime maintenance.

Documentation
-------------

Currently the only documentation is this README, but there is an
ongoing process to document roles with their own READMEs.
