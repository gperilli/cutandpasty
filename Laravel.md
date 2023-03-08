## Laravel

### Database management
```
php artisan migrate:fresh --seed

```

```
php artisan migrate:refresh
```

```
php artisan db:seed --class=AppleInspectionSeeder
```

```
php artisan db:wipe
```


### Logging stuff

```
info()
```

```
dd()
```


### Dates and Time

```
Carbon::now()->toDateTimeString();
```

### Models and Instnces

```
$posts = Post::all();
```

### Server side HTML rendering

```
@if()
@elseif ()
@endif
```

```
@foreach($channels as $key => $channel)
@endforeach
```
