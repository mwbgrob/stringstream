# Php StringStream

[![Latest Stable Version](http://poser.pugx.org/golding/ascii-table/v)](https://packagist.org/packages/golding/ascii-table) [![Total Downloads](http://poser.pugx.org/golding/ascii-table/downloads)](https://packagist.org/packages/golding/ascii-table) [![Latest Unstable Version](http://poser.pugx.org/golding/ascii-table/v/unstable)](https://packagist.org/packages/golding/ascii-table) [![License](http://poser.pugx.org/golding/ascii-table/license)](https://packagist.org/packages/golding/ascii-table) [![PHP Version Require](http://poser.pugx.org/golding/ascii-table/require/php)](https://packagist.org/packages/golding/ascii-table)

Php Stringstream data structure.

## Installation

```shell
composer require golding/stringstream
```

## Usage
```php
<?php
    use Golding\stringstream\StringStream;
    
    require(__DIR__ . '/vendor/autoload.php');
    
    $stream = new StringStream("Hello, World!");
    
    do {
        if($stream->currentAscii()->isWhiteSpace()) {
            $stream->ignoreWhitespace();
        } else {
            echo $stream->current().PHP_EOL;
            $stream->next();
        }
    
    } while (! $stream->isEnd());

```

## License
released under the MIT License.
See the [bundled LICENSE file](LICENSE) for details.
