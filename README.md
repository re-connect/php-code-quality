# php-code-quality
Small sub package used to check code quality on a Symfony project

## Tools

* Php-cs-fixer
* Phpstan
* PhpMd

### Setup

```bash
git clone git@github.com:re-connect/php-code-quality.git
cd php-code-quality
symfony composer install
cd ../
```

### Run

#### Php-cs-fixer

```bash
php-code-quality/vendor/bin/php-cs-fixer fix src
php-code-quality/bin/php-cs-fixer fix tests
```

#### Phpstan

```bash
php-code-quality/vendor/bin/phpstan analyse -l 0 -c php-code-quality/phpstan.neon src
php-code-quality/vendor/bin/phpstan analyse -l 0 -c php-code-quality/phpstan.neon tests
```

#### Php-md

```bash
php-code-quality/vendor/bin/phpmd src text codesize,unusedcode,naming,cleancode,controversial,design
php-code-quality/vendor/bin/phpmd tests text codesize,unusedcode,naming,cleancode,controversial,design
```


