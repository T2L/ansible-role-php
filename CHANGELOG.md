## Ansible Role: PHP (Unreleased)

- [#22](https://github.com/T2L/ansible-role-php/issues/22) - Drop Ubuntu 16.04 support
- Explicitly require yamllint on Travis CI

## Ansible Role: PHP 1.4.0, 2021-03-02

- Bump the default PHP version to 7.4
- [#19](https://github.com/T2L/ansible-role-php/issues/19) - Make Travis CI happy again (improve testing setup)

## Ansible Role: PHP 1.3.1, 2020-08-20

- [#18](https://github.com/T2L/ansible-role-php/issues/18) - Address newly introduced Ansible Lint "[208] File permissions not mentioned" message. Update Travis configuration (new Ansible version)

## Ansible Role: PHP 1.3.0, 2020-04-27

- [#14](https://github.com/T2L/ansible-role-php/issues/14) - Add Ubuntu 20.04 support (testing with PHP 7.4)
- [#13](https://github.com/T2L/ansible-role-php/issues/13) - Add Molecule 3 support

## Ansible Role: PHP 1.2.1, 2020-01-14

- [GH-11](https://github.com/T2L/ansible-role-php/issues/11) - Run Travis on 1.x.x, tagged releases and PR only
- [GH-5](https://github.com/T2L/ansible-role-php/issues/5) - Bump the default PHP version to 7.3 (for real)

## Ansible Role: PHP 1.2.0, 2020-01-13

- [GH-5](https://github.com/T2L/ansible-role-php/issues/5) - Bump the default PHP version to 7.3
- [GH-8](https://github.com/T2L/ansible-role-php/issues/8) - Apache2 and CLI will be using a proper PHP version upon changing the one

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
