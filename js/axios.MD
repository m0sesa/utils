# [php server that can receive json]

##### GET 

```javascript
axios.get('https://example.com/endpoint.php',
    {
        params: {
            param1: "value1",
            param2: "value2",
        }
    })
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
```

##### POST

```javascript
axios(
    {
        method: 'post',
        url: 'https://example.com/endpoint.php',
        data: {
            data1: 'Data1',
            data2: 'Data2'
        }
    })
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
```

##### PUT

```javascript
axios(
    {
        method: 'put',
        url: 'https://example.com/endpoint.php',
        data: {
            data1: 'Data1',
            data2: 'Data2'
        }
    })
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
```

##### PATCH

```javascript
axios(
    {
        method: 'patch',
        url: 'https://example.com/endpoint.php',
        data: {
            data1: 'Data1',
            data2: 'Data2'
        }
    })
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
```

##### DELETE

```javascript
axios(
    {
        method: 'delete',
        url: 'https://example.com/endpoint.php',
        data: {
            data1: 'Data1',
            data2: 'Data2'
        }
    })
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
```
