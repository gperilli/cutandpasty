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

### MVC Routing

routes
```
routes/web.php
```


### Dates and Time
https://carbon.nesbot.com/docs/

```
Carbon::now()->toDateTimeString();
```

### Models and Instnces

get all
```
$posts = Post::all();
```

wipe all
```
DB::table('users')->truncate();
```

update
```
$user->update(['password' => $userPassword]);
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

#### send variables from controller to blade file
```
return view('client/facility/graph/cbm/vherme/facilityInspectionGraph')->with([
            'facility' => $facility,
            'test' => $test,
        ]);
```


