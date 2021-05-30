# Send array and objects with AJAX from jQuery to PHP

To send objects from jQuery to PHP is necessary to encode in JSON format.

* On jQuery:
``
JSON.Stringify(object)
``
* On PHP:
```php
json_decode(html_entity_decode(stripslashes($_POST)));
```
