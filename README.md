# PHPCS <inclue-pattern> demo repo

This little repo can reproduce my issue with PHPCS not adhering to the defined include-patterns.

## Usage

```
composer install
composer test
composer run basic
composer run verbose
```

This replicates my basic WordPress setup. I've included a small plugin and an example vendor file `ignore-me.php` that should be ignored. by the ruleset.

PHPCS is still running on files it shouldn't unless I explicitly exclude every file and directory that is not mine, which is getting old.
The basic.xml ruleset responds with an error code 1 which is likely a seperate issue.

Original issue:
https://github.com/squizlabs/PHP_CodeSniffer/issues/2177#issuecomment-427692498
