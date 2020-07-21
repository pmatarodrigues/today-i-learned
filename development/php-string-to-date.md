# PHP - Convert String to Date


```
$date = '22/09/1922';
$date = str_replace('/', '-', $date);
echo date('Y-m-d', strtotime($date));
```

> Dates in the m/d/y or d-m-y formats are disambiguated by looking at the separator between the various components: if the separator is a slash (/), then the American m/d/y is assumed; 
> Whereas if the separator is a dash (-) or a dot (.), then the European d-m-y format is assumed.
