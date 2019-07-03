## Custom Paginator

http://psampaz.github.io/custom-data-pagination-with-laravel-5/

```php
<?php namespace App\Http\Controllers;

use Illuminate\Pagination\LengthAwarePaginator;
use Illuminate\Support\Collection;

class SearchController extends Controller {

    public function search()
    {
        .
        .
        .

        $searchResults = [
            'item1',
            'item2',
            'item3',
            'item4',
            'item5',
            'item6',
            'item7',
            'item8',
            'item9',
            'item10'
            ];

        //Get current page form url e.g. &page=6
        $currentPage = LengthAwarePaginator::resolveCurrentPage();

        //Create a new Laravel collection from the array data
        $collection = new Collection($searchResults);

        //Define how many items we want to be visible in each page
        $perPage = 5;

        //Slice the collection to get the items to display in current page
        $currentPageSearchResults = $collection->slice($currentPage * $perPage, $perPage)->all();

        //Create our paginator and pass it to the view
        $paginatedSearchResults= new LengthAwarePaginator($currentPageSearchResults, count($collection), $perPage);

        return view('search', ['results' => $paginatedSearchResults]);
    }
?>
```


```sh
sudo chown -R www-data:www-data .
sudo find .  -type f -exec chmod 644 {} \;
sudo find . -type d -exec chmod 755 {} \;
sudo chgrp -R www-data storage bootstrap/cache
sudo chmod -R ug+rwx storage bootstrap/cache
 
```

## Fix tinker on mac

```
vim ~/.config/psysh/config.php
```

```php
return [
  'usePcntl' => false,
];
```

