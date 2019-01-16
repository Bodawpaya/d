## Routate Log

**Within Server Block >> **

```
if ($time_iso8601 ~ "^(\d{4})-(\d{2})-(\d{2})") {
	set $year $1;
	set $month $2;
	set $day $3;
}

access_log /var/log/nginx/$year-$month-$day-access.log;
```
