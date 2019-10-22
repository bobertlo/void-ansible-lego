lego
====

What is does this role do?
--------------------------

This role installs and configures lego to obtain certificates
automatically from an ACME CA.

> NOTE: setting `nginx_acme_challenge_path` will be needed to
> use the void nginx ansible role to answer challenges.

Meta
----

Files Managed:
  * /var/lib/lego/*
  * /usr/libexec/{register,renew}
  * /etc/cron.d/lego

Defaults Provided:
  * lego_webroot: /var/run/lego/webroot
  * lego_user: _lego
  * lego_group: nginx

Variables Required:
  * lego.hostmaster_email: Email address for alerts
  * lego.sites: list of site urls

Optional Variables:
  * None

Files Required:
  * None

Optional Files:
  * None

Conflicting Roles:
  * None

Depends On:
  * None
