# PHP-route
A PHP Route Class

## How to use ?

To use PHP Router Class you need to clone our repository. Considering you've already made it, make a file .php as you preferer.

This example doesn't use PSR4/0 however we are using namespace, i recommend you to keep it.

Put the code below in your file .php

    use \Src\Core\Router;

    Router::route('/', function(){	
      echo "You're in home page";
    });
    Router::execute($_SERVER['REQUEST_URI']);
    
To every created router you need re-execute the router as you seen above. The next example show how you can use regex pattern.

use \Src\Core\Router;

Router::route("/(\w+)/", function($id){	
  echo 'My id is: {$id}';
});
Router::execute($_SERVER['REQUEST_URI']);
