# Ansible Role: PHP

[![Build Status](https://travis-ci.org/T2L/ansible-role-php.svg?branch=1.1.0)](https://travis-ci.org/T2L/ansible-role-php)

Installs PHP on Ubuntu LTS using [The main PPA for PHP](https://launchpad.net/~ondrej/+archive/ubuntu/php).

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](defaults/main.yml)):

PHP version to install:

    php_version: 7.1

PHP extensions to install. Specify naked extension names (i.e. do not include PHP version), for example `mbstring`:

    php_extensions: []

PHP configuration directives. PHP used with Apache and CLI PHP must be configured separately using corresponding variables:

    php_configuration: {}
    php_cli_configuration: {}

PHP stores it's configuration in INI files. Main `php.ini` file contains several sections, individual keys (properties) belong to a certain section.

The same pattern applies to the configuration variables. It's a nested dictionary, where the first level represents name of a section. The second level is a dictionary of PHP directives and their values.

Example:

    php_configuration:
      Date:
        date.timezone: Europe/Kiev
      PHP:
        memory_limit: 256M
        upload_max_filesize: 64M
        post_max_size: 512M

PHP extensions which use own ini files should be configured using (not all extensions actually do that). Actually some of them uses main php.ini for storing configuration (e.g. opcache):

    php_extensions_configuration: {}

This variable follows the same format as main one described above (nested dictionary), except section represent the extension itself.

Example:

    php_extensions_configuration:
      ldap:
        ldap.max_links: 5
      xdebug:
        xdebug.remote_enable: 'On'

Web server daemon. Will be restarted when change in configuration is detected. Defaults to Apache 2:

    php_web_server_daemon: apache2

Boolean indicating whether to restart web server or not:

    php_restart_web_server: true

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - T2L.php

## License

MIT

## Author Information

This role was created in 2017 by Roman Paska.

## Changelog

Changelog can be found here [CHANGELOG.md](CHANGELOG.md)
