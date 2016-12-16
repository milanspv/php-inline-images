# inline-images

A PHP lib to handle image inlining in your (css, img src, etc.)

# Install
```bash
composer require milanspv/php-inline-images
```

# Convert an image to an inline string value

```php
<?php

// first way to initialize the object
$inliner = new InlineImages\Converter();
$inliner->setPath('/path/to/img.png');

// second way to initialize the object
$inliner = new InlineImages\Converter('/path/to/img.png');

// convert image
echo '<img src="'.$inliner->convert().'"/>';
//or for css
echo 'background: url('.$inliner->convert().')';

```

# Convert a remote image to inline string value
```php
<?php

$inliner = new InlineImages\Converter('http://path/to/img.png');

echo '<img src="'.$inliner->convert().'"/>';
//or for css
echo 'background: url('.$inliner->convert().')';

```

# Inline SVGs
```php
<?php

$inliner = new InlineImages\Converter('/path/to/img.svg');

echo '<img src="'.$inliner->convert().'"/>';
//or for css
echo 'background: url('.$inliner->convert().')';

```