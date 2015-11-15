# php-date

## getting started  
``` 
include 'Date.php';  
use Prototypeblocks\Date;  
``` 
## examples  
#### difference
Formats: seconds, minutes, hours, days, months, years  
``` 
$date1 = '2016-01-01';
$difference = Date::difference($date1);
// $differnece is difference in seconds between 1st of january 2016 and now 
``` 
``` 
$date1 = '2016-01-01';
$date2 = '2016-01-02';
$difference = Date::difference($date1, $date2);
// $differnece is difference in seconds between 1st of january 2016 and 2nd of january 2016
``` 
``` 
$date1 = '2016-01-01';
$date2 = '2016-01-02';
$difference = Date::difference($date1, $date2, 'hours');
// $differnece is difference in hours between 1st of january 2016 and 2nd of january 2016
``` 
#### format
``` 
$formattedDate = Date::format('2015-11-15 10:10:00', 'Y-m-d');
// $formattedDate is date in Y-m-d format, 2015-11-15
``` 
#### now
``` 
$now = Date::now();
// $now is current date, default format is Y-m-d H:i:s
``` 
``` 
$now = Date::now('Y-m-d');
// $now is current date in Y-m-d format
``` 
#### isDate
``` 
$boolean = Date::isDate('2015-11-15 10:10:00');
// $boolean is true, as the default checked format is Y-m-d H:i:s
``` 
``` 
$boolean = Date::isDate('2015-11-15 10:10:00', 'Y-m-d);
// $boolean is false, as the given date does not match the given format 
``` 
#### isValid  
Is alias for Date::isDate  
#### setTimezone
``` 
Date::setTimezone();
// Will set timezone to UTC 
``` 
``` 
Date::setTimezone('Europe/Amsterdam');
// Will set timezone to Amsterdam 
``` 
