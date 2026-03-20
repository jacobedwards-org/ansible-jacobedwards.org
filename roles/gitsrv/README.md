Ansible gitsrv role
===================

The gitsrv role installs and configures
[gitsrv](https://jacobedwards.org/projects/gitsrv).

Variables
---------

The role can be configured with the following variables:

- `gitsrv_user` — User running gitsrv.
- `gitsrv_conf` — Options for gitsrv.
- `gitsrv_stagit_styles` — Directory containing stagit styles.

The `gitsrv_conf` is a map of key/value pairs. Valid options listed below:

- `pubfile` — Configures which repositories gitsrv considers public.
- `distdir` — Enable tag tarball generation and set export directory.
- `mandir` — Enable manpage exports and set output directory.
- `github_token` — Enable GitHub mirroring and set the PAT token.
- `stagit_enable` — Enable stagit-hook in gitsrv.
- `stagit_baseurl` — Set stagit-hook baseurl option. 
- `stagit_basedir` — Set stagit-hook basedir option. 
- `stagit_repodir` — Set stagit-hook basedir option. 
- `stagit_styledir` — Set stagit-hook basedir option. (Default
  `/etc/stagit-styles`).

These options mostly map to stagit.conf(5) and stagit-hook.conf(5)
configuration options.
