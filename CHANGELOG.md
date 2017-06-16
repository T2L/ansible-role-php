## Ansible Role: PHP 1.x.x

## Ansible Role: PHP 1.1.0, 2017-06-16

- Added support of configuring PHP extensions, which use own ini files (say hello to xdebug):
    * Introduced new variable: `php_extensions_configuration` (empty by default). It follows the same nested format as other configuration variables (`php_configuration` and `php_cli_configuration`)

## Ansible Role: PHP 1.0.0, 2017-05-24

- Initial release, nothing fancy
