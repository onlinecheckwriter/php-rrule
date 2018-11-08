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
```




# JAVASCRIPT RRULE TEXT TO PHP DATE WITH DTSTART
```php
$data = "FREQ=DAILY;DTSTART=2018-11-25;INTERVAL=1;UNTIL=2018-11-30";

$one = explode(";",$data);

$ru=null;
foreach($one as $a)
{
	
	$b=explode("=",$a);
	$ru[$b[0]] = $b[1];
	
	

}


$rrule = new RRule($ru);
$i=0;
foreach ( $rrule as $occurrence ) {
	echo $occurrence->format('Y-m-d'),", <br>";
	//
	$i++;
	if($i>200)
	{
		
		break;
		
	}
	
}

```
