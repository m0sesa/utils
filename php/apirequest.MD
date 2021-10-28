# [Requests with json body]

```php

$requestType = $_SERVER['REQUEST_METHOD'];

$requestUrl = $_SERVER['REQUEST_URI'];
$url_components = parse_url($url);

$json = file_get_contents('php://input');
$requestData = json_decode($json);

if ($requestType == 'GET'){
  $params = $_GET;
  // Continue
}else if ($requestType == 'POST'){
  $data = $requestData;
  // Continue
}else if ($requestType == 'PATCH'){
  $data = $requestData;
  // Continue
}else if ($requestType == 'PUT'){
  $data = $requestData;
  // Continue
}else if ($requestType == 'DELETE'){
  $data = $requestData;
  // Continue
}

```
