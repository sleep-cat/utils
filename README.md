AlphaSnow/Utils
===========
[![Latest Stable Version](https://poser.pugx.org/alphasnow/utils/v/stable)](https://packagist.org/packages/alphasnow/utils)
[![Total Downloads](https://poser.pugx.org/alphasnow/utils/downloads)](https://packagist.org/packages/alphasnow/utils)
[![License](https://poser.pugx.org/alphasnow/utils/license)](https://packagist.org/packages/alphasnow/utils)
[![Build Status](https://travis-ci.org/alphasnow/utils.svg?branch=master)](https://travis-ci.org/alphasnow/utils)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/alphasnow/utils/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/alphasnow/utils/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/alphasnow/utils/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/alphasnow/utils/?branch=master)

## Requirement
- PHP >= 7.2

## Install
```bash
composer require alphasnow/utils
```

## Example
```php
use AlphaSnow\Utils\ListTree;
$list = [
    ['id' => 1, 'pid' => 0, 'name' => 'node1'],
    ['id' => 2, 'pid' => 1, 'name' => 'node2'],
    ['id' => 3, 'pid' => 2, 'name' => 'node3'],
];
$tree = ListTree::listToTree($list);
/*
[
    ['id' => 1, 'pid' => 0, 'name' => 'node1', '_child' => [
        ['id' => 2, 'pid' => 1, 'name' => 'node2', '_child' => [
            ['id' => 3, 'pid' => 2, 'name' => 'node3']
        ]]
    ]],
];
*/

$name = snake_name('ArticleCategory')
// article_category
```

## scripts
```bash
# composer exec --list

# Fix PHP code style
composer exec php-cs-fixer

# PHP Static Analysis
composer exec phpstan
```

## Credits

- [AlphaSnow][link-author]

## License
MIT License. See the [LICENSE](LICENSE.txt) file.


[link-author]: https://github.com/alphasnow