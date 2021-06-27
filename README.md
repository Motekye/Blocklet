# blocklet

Create block letter comments for code.

Includes several typefaces, all 4 lines tall. Typefaces vary in width from 3 to 6 characters, all monospace.

## using PHP version

```
<?php
include "blocklet.php";
$blocklet = new Blocklet;
echo "<pre>".$blocklet->create(
	$_SERVER["QUERY_STRING"], 
	true
)."</pre>";
```

Use the above snippet to create a block header from the querystring sent on a request.
The 'create' function takes two parameters; the first being the quote to print in the block header and the second defining whether the output should be HTML formatted.
