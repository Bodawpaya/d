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

https://www.if-not-true-then-false.com/2011/nginx-and-php-fpm-configuration-and-optimizing-tips-and-tricks/comment-page-2/#comments
