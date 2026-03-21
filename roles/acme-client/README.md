Ansible acme-client role
========================

This role configures acme-client for support for multiple domains
and alternate names.

Variables
---------

The following variables can be configured for the role:

- `acmeclient_refresh_command` — Command run when the acme-client
  configuration changes. (Default `autocert`.)

- `acmeclient_cert_root` — Root for TLS certificates. (Default
  `/etc/ssl`.)

- `acmeclient_acme_root` — Root for acme keys. (Default `/etc/acme`.)

- `acmeclient_authority_keyfile` — Secret key for the authority.
  (No default. Required.)

- `acmeclient_authority_name` — Name of authority. (Default
  `letsencrypt`.)

- `acmeclient_authority_url` — Authority api url. (Default
  `https://acme-v02.api.letsencrypt.org/directory`.)

- `acmeclient_mailto` — Email for the authority to contact. (Default
  `hostmaster@{{ ansible_host }}`.)

- `acmeclient_certs` — Map of handles/domains and their alternate
   names. (Default `[]`.)

Here is an example value for `acmeclient_certs`:

	example.com:
	  www.example.com
	  ftp.example.com
