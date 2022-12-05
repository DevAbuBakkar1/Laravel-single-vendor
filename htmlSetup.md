#### Step O1 : Basic Setup :- 
- Keep All HTML files is Public Folder making Admin or Frondend Folder : 
- Separate Files in Views 
- Create Middleware and Add code in Middle Ware : 
```
  if(auth()->user()->role == 1){
            return $next($request);
        }
```
- Add Role in user from database migration
```
$table->string('role')->default(0);
```

- Set Middleware in Karnel 
```
'AdminMiddleware' => \App\Http\Middleware\AdminMiddleware::class,
```

- Create Admin Controller  and make it auth check :
```
 public function __construct()
        {
            $this->middleware('auth');
        }
}
```
- Create New Route 
```
<?php
use Illuminate\Support\Facades\Route;
```
- Use 




