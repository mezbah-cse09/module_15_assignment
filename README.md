# module_15_assignment

Create a `get` route called `/profile` with a required parameter `id`, which will connect to a controller named `ProfileController`. This ProfileController should have only one public method called `index`.


The `index` method will receive the `$id` as a route parameter.  Inside the `index` method declare two variables called `$name` and set the value “Donal Trump” and the `$age` value will be “75”. The values of both variables must be in double quotation.


Then make a `$data` variable to store the `$id` as well as the declared variables $name and $age as an associative array. The name of the keys will be the same.


Also make a cookie; name as `access_token` , value  as `123-XYZ` , minutes as 1, path as ‘/’, domain as $_SERVER[‘SERVER_NAME’], secure as false and httpOnly as true.


Return this data as response with status-code `200` and cookie.


*Note that the template is only for your understanding purpose. Do not just copy paste this template in your project. Make necessary changes like renaming the variables, route, method and complete the whole task according to the question. Also do not add the template’s comment in your file/code. Those are just instructions.


====Template  Starts======


```

Route File:


<?php
use Illuminate\Support\Facades\Route;


use App\Http\Controllers\ProfileController;


Route::get('/yourRouteName/{yourRequiredParameter}’, [YourController::class, 'yourMethod']);



Controller File:


<?php


namespace App\Http\Controllers;



class ProfileController extends Controller


{


public function index($yourRequiredParameter){


// Declare your variables and assign the values stated in Question


   $name = “” ;


   $age = “” ;


//add three variables in $data variable as associative array with values stated in the question


   $data = [


…….


…….


……


   ];


//Set your cookie variables stated in the question


$name = ‘’;


$value = ‘’;


$minutes = ‘’;


$path = ‘’;



$domain = ‘’;


$secure = ‘’;


$httpOnly = ‘’;


   //add the return statement with the response method along with $data and status-code and set the cookie stated in the question.


………


………


}


}


=====Template  Ends=====
Expected Output


=====================


(No Need to add the output in your answer, not even by commenting. This is just for you, to check if your code is working correctly or not):


 


{


     "id": "yourRequiredParameter", (It can be any number what is passed in the route)


     "name": "Donal Trump",



     "age": "75"


}


Also check whether the cookie is set properly.

```