# Send array and objects with AJAX from jQuery to PHP

To send objects from jQuery to PHP is necessary to encode in JSON format.

* On jQuery:
``
JSON.Stringify(object)
``
* On PHP:
``
json\_decode(html\_entity\_decode(stripslashes($POST)));
``
