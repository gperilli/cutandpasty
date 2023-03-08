## Laravel

### Database management

#### Seeding and Wiping
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

#### Migrating

```
php artisan make:migration add_paid_to_users_table --table=users
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
