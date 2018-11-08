# RRULE for PHP

## Basic example

```php
use RRule\RRule;

$rrule = new RRule([
	'FREQ' => 'MONTHLY',
	'INTERVAL' => 1,
	'DTSTART' => '2015-06-01',
	'COUNT' => 6
]);

foreach ( $rrule as $occurrence ) {
	echo $occurrence->format('D d M Y'),", ";
}

#convert Rrules string 
