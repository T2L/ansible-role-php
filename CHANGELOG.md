## Ansible Role: PHP 1.1.2, 2019-01-17

- [GH-2](https://github.com/T2L/ansible-role-php/issues/2) - Fixed deprecation warning regarding running apt using a loop (Ansible 2.7+)
- [GH-4](https://github.com/T2L/ansible-role-php/issues/4) - Updated Travis.CI configuration

## Ansible Role: PHP 1.1.1, 2017-07-03

- Fix broken Travis CI (Package 'docker-engine' has no installation candidate)

## Ansible Role: PHP 1.1.0, 2017-06-16

- Added support of configuring PHP extensions, which use own ini files (say hello to xdebug):
    * Introduced new variable: `php_extensions_configuration` (empty by default). It follows the same nested format as other configuration variables (`php_configuration` and `php_cli_configuration`)

## Ansible Role: PHP 1.0.0, 2017-05-24

- Initial release, nothing fancy
