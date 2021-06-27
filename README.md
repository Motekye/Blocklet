# blocklet

Create block letter comments for code.

Includes several typefaces, all 4 lines tall. Typefaces vary in width from 3 to 6 characters.

```
/******************************************************************************/
/*** .####_ .####, ##   # #####_ ##     ###### ********************************/
/*** ##__ ^ ##   # ### ## ##  .# ##     ##___  ********************************/
/*** __^^## ###### ## * # #####^ ##     ##^^^  ********************************/
/*** *####  ##   # ##   # ##     ###### ###### ********************************/
/******************************************************************************/
```

Comes with the typefaces: ** 6, 5, 5l, 4l, 4xl, 3, 3l, 3xl **

## using PHP version

```
<?php
include "blocklet.php";
$blocklet = new Blocklet;
echo "<pre>".$blocklet->create(
	$_SERVER["QUERY_STRING"],
	'6',
	true
)."</pre>";
```

Use the above snippet to create a block header from the querystring sent on a request.
The 'create' function takes three parameters; the first being the quote to print in the block header, the second being the name of the typeset to use as a string and the third defining whether the output should be HTML formatted.
