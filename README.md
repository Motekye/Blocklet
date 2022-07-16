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

Comes with the typefaces: 6, 5, 5l, 4l, 4xl, 3, 3l, 3xl
Only letters, numbers, spaces and hyphens are allowed in the quote. All other characters are substituted with hyphens.

## using PHP version

```
<?php
include "path/to/blocklet.php";
echo "<pre>".Blocklet::create(
	$_SERVER["QUERY_STRING"],
	'6',
	true
)."</pre>";
```

Use the above snippet to create a block header from the querystring sent on a request.
The 'create' function takes three parameters; the first being the quote to print in the block header, the second being the name of the typeset to use as a string and the third defining whether the output should be HTML formatted.

## using Javascript version

```
<script src="/path/to/blocklet.js"></script>
<script>
var pre = document.getElementById('my-pre');
BLOCKLET.col_width = 80;
pre.textContent = BLOCKLET.create(
	'Caption',
	'6'
);
</script>
```

Use the above code to paste the block header into a \<pre> element with the id "my-pre". Change the code as needed.

The javascript version of this module doesn't take the HTMLescaped parameter, as assigning to the textContent of an element will do this for you automatically. Otherwise the parameters are the same as the PHP version.
