```php

$servername = 'localhost';
$username = 'root';
$password = '';
$dbname = 'test';

try{
    $conn = new mysqli($servername, $username, $password, $dbname);
}catch(Exception $e){
    die('Error......');
}

function getResource(array $params){
    global $conn;

    $query = "SELECT * FROM test WHERE col1 = ? AND col2 = ?";
    $stmt = $conn->prepare($query);
    $stmt->bind_param("ss", $params['col1'], $params['col2']);
    $stmt->execute();

    $result = $stmt->get_result();
    
    $array = [];
    if ($result->num_rows != 0){
        while($row = $result->fetch_object()){
            array_push($array, $row);
        }
    }
    return $array;
}

function insertResource(array $params){
    global $conn;

    $query = "INSERT INTO test ('col1', 'col2') VALUES (?, ?) ";
    $stmt = $conn->prepare($query);
    $stmt->bind_param("ss", $params['col1'], $params['col2']);

    if ($stmt->execute()) {
        return $conn->insert_id;
    } else {
        return -1;
    }
}

function updateResource(array $params){ // sames goes for deleting a resource too
    global $conn;

    $query = "UPDATE test SET col1 = ? WHERE col2 = ? ";
    $stmt = $conn->prepare($query);
    $stmt->bind_param("ss", $params['col1'], $params['col2']);

    if ($stmt->execute()) {
        return $conn->affected_rows;
    } else {
        return -1;
    }
}

```
