---
title: "Rest APIs"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "nodes"
weight: 304
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Authentication

- HTTP Authentication, scheme: basic Basic Authorization header using the Bearer scheme.

<h1 id="andy-x-activities">Activities</h1>

### get__api_v3_activities_tenants_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/tenants/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/tenants/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/tenants/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/tenants/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/tenants/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/tenants/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/tenants/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/tenants/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/tenants/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_tenants_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_products_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/products/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/products/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/products/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/products/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/products/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/products/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/products/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/products/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/products/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_products_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_components_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/components/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/components/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/components/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/components/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/components/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/components/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/components/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/components/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/components/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_components_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_topics_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/topics/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/topics/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/topics/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/topics/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/topics/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/topics/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/topics/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/topics/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/topics/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_topics_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_subscriptions_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/subscriptions/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/subscriptions/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/subscriptions/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/subscriptions/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/subscriptions/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/subscriptions/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/subscriptions/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/subscriptions/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/subscriptions/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_subscriptions_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_producers_count

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/producers/count \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/producers/count HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/producers/count',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/producers/count',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/producers/count', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/producers/count', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/producers/count");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/producers/count", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/producers/count`

> Example responses

> 200 Response

```json
0
```

<h3 id="get__api_v3_activities_producers_count-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_subscriptions

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/subscriptions \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/subscriptions HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/subscriptions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/subscriptions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/subscriptions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/subscriptions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/subscriptions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/subscriptions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/subscriptions`

> Example responses

> 200 Response

```json
[
  {
    "name": "string",
    "location": "string",
    "isActive": true
  }
]
```

<h3 id="get__api_v3_activities_subscriptions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_activities_subscriptions-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[SubscriptionActivity](#schemasubscriptionactivity)]|false|none|none|
|» name|string¦null|false|none|none|
|» location|string¦null|false|none|none|
|» isActive|boolean|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_activities_producers

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/activities/producers \
  -H 'Accept: application/json'

```

```http
GET /api/v3/activities/producers HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/activities/producers',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/activities/producers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/activities/producers', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/activities/producers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/activities/producers");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/activities/producers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/activities/producers`

> Example responses

> 200 Response

```json
[
  {
    "key": "string",
    "tenant": "string",
    "name": "string",
    "location": "string",
    "isActive": true,
    "instancesCount": 0
  }
]
```

<h3 id="get__api_v3_activities_producers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_activities_producers-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ProducerActivity](#schemaproduceractivity)]|false|none|none|
|» key|string¦null|false|none|none|
|» tenant|string¦null|false|none|none|
|» name|string¦null|false|none|none|
|» location|string¦null|false|none|none|
|» isActive|boolean|false|none|none|
|» instancesCount|integer(int32)|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-clusters">Clusters</h1>

### get__api_v3_clusters

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/clusters \
  -H 'Accept: application/json'

```

```http
GET /api/v3/clusters HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/clusters',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/clusters',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/clusters', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/clusters', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/clusters");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/clusters", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/clusters`

> Example responses

> 200 Response

```json
{
  "inThroughputInMB": 0,
  "outThroughputInMB": 0,
  "activeDataIngestions": 0,
  "activeSubscriptions": 0,
  "name": "string",
  "shardDistributionType": "Sync",
  "status": "Online",
  "shards": [
    {
      "replicaDistributionType": "Sync",
      "replicas": [
        {
          "nodeId": "string",
          "host": "string",
          "port": "string",
          "connectionType": "SSL",
          "username": "string",
          "password": "string",
          "type": "Main",
          "isConnected": true,
          "isLocal": true,
          "x509CertificateFile": "string",
          "x509CertificatePassword": "string"
        }
      ]
    }
  ]
}
```

<h3 id="get__api_v3_clusters-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Cluster](#schemacluster)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_clusters_nodes_current

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/clusters/nodes/current \
  -H 'Accept: application/json'

```

```http
GET /api/v3/clusters/nodes/current HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/clusters/nodes/current',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/clusters/nodes/current',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/clusters/nodes/current', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/clusters/nodes/current', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/clusters/nodes/current");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/clusters/nodes/current", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/clusters/nodes/current`

> Example responses

> 200 Response

```json
{
  "nodeId": "string",
  "host": "string",
  "port": "string",
  "connectionType": "SSL",
  "username": "string",
  "password": "string",
  "type": "Main",
  "isConnected": true,
  "isLocal": true,
  "x509CertificateFile": "string",
  "x509CertificatePassword": "string"
}
```

<h3 id="get__api_v3_clusters_nodes_current-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Replica](#schemareplica)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-components">Components</h1>

### get__api_v3_tenants_{tenant}_products_{product}_components

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Component](#schemacomponent)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}`

> Body parameter

```json
{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|description|query|string|false|none|
|body|body|[ComponentSettings](#schemacomponentsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component} \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}`

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|description|query|string|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_components_{component}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/components/{component}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/components/{component}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/components/{component}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/components/{component}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[ComponentSettings](#schemacomponentsettings)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/settings`

> Body parameter

```json
{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|body|body|[ComponentSettings](#schemacomponentsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "issuedFor": "string",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens`

> Body parameter

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "issuedFor": "string",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|body|body|[ComponentToken](#schemacomponenttoken)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "roles": [
      "Produce"
    ],
    "isActive": true,
    "expireDate": "2019-08-24T14:15:22Z",
    "issuedFor": "string",
    "description": "string",
    "issuedDate": "2019-08-24T14:15:22Z",
    "updatedDate": "2019-08-24T14:15:22Z",
    "createdDate": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "createdBy": "string"
  }
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ComponentToken](#schemacomponenttoken)]|false|none|none|
|» id|string(uuid)|false|none|none|
|» roles|[[ComponentTokenRole](#schemacomponenttokenrole)]¦null|false|none|none|
|» isActive|boolean|false|none|none|
|» expireDate|string(date-time)|false|none|none|
|» issuedFor|string¦null|false|none|none|
|» description|string¦null|false|none|none|
|» issuedDate|string(date-time)|false|none|none|
|» updatedDate|string(date-time)¦null|false|none|none|
|» createdDate|string(date-time)|false|none|none|
|» updatedBy|string¦null|false|none|none|
|» createdBy|string¦null|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}_revoke

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}/revoke`

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}_revoke-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|key|path|string(uuid)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}_revoke-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/tokens/{key}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|key|path|string(uuid)|true|none|

> Example responses

> 200 Response

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "issuedFor": "string",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_tokens_{key}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[ComponentToken](#schemacomponenttoken)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "name": "string",
    "type": "SOFT_TTL",
    "timeToLiveInMinutes": 0,
    "updatedDate": "2019-08-24T14:15:22Z",
    "createdDate": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "createdBy": "string"
  }
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ComponentRetention](#schemacomponentretention)]|false|none|none|
|» id|integer(int64)|false|none|none|
|» name|string¦null|false|none|none|
|» type|[RetentionType](#schemaretentiontype)|false|none|none|
|» timeToLiveInMinutes|integer(int64)|false|none|none|
|» updatedDate|string(date-time)¦null|false|none|none|
|» createdDate|string(date-time)|false|none|none|
|» updatedBy|string¦null|false|none|none|
|» createdBy|string¦null|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|type|SOFT_TTL|
|type|HARD_TTL|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|body|body|[ComponentRetention](#schemacomponentretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|id|path|integer(int64)|true|none|
|body|body|[ComponentRetention](#schemacomponentretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/retentions/{id}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-node">Node</h1>

### get__api_v3_node_version

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/node/version \
  -H 'Accept: text/plain'

```

```http
GET /api/v3/node/version HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v3/node/version',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.get '/api/v3/node/version',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.get('/api/v3/node/version', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/node/version', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/node/version");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/node/version", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/node/version`

> Example responses

> 200 Response

```
{"name":"string","shortName":"string","version":"string"}
```

```json
{
  "name": "string",
  "shortName": "string",
  "version": "string"
}
```

<h3 id="get__api_v3_node_version-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[ApplicationDetails](#schemaapplicationdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_node_users_role

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/node/users/role \
  -H 'Accept: text/plain'

```

```http
GET /api/v3/node/users/role HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v3/node/users/role',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.get '/api/v3/node/users/role',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.get('/api/v3/node/users/role', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/node/users/role', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/node/users/role");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/node/users/role", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/node/users/role`

> Example responses

> 200 Response

```
"string"
```

```json
"string"
```

<h3 id="get__api_v3_node_users_role-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-producers">Producers</h1>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|producer|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "instanceType": "Single",
  "publicIpRange": [
    "string"
  ],
  "privateIpRange": [
    "string"
  ],
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Producer](#schemaproducer)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}`

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|producer|path|string|true|none|
|description|query|string|false|none|
|instanceType|query|[ProducerInstanceType](#schemaproducerinstancetype)|false|none|

##### Enumerated Values

|Parameter|Value|
|---|---|
|instanceType|Single|
|instanceType|Multiple|

> Example responses

> 200 Response

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Subscription](#schemasubscription)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/producers/{producer}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|producer|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_producers_{producer}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Subscription](#schemasubscription)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-products">Products</h1>

### get__api_v3_tenants_{tenant}_products

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products`

<h3 id="get__api_v3_tenants_{tenant}_products-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_products-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Product](#schemaproduct)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isAuthorizationEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}`

> Body parameter

```json
{
  "isAuthorizationEnabled": true
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|description|query|string|false|none|
|body|body|[ProductSettings](#schemaproductsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product} \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}`

<h3 id="put__api_v3_tenants_{tenant}_products_{product}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|description|query|string|false|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Product](#schemaproduct)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_delete

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/delete \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/delete HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/delete',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/delete',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/delete', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/delete', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/delete");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/delete", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/delete`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_settings

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/settings \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/settings HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/settings',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/settings`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "isAuthorizationEnabled": true
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[ProductSettings](#schemaproductsettings)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_settings

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/settings \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/settings HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isAuthorizationEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/settings',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/settings`

> Body parameter

```json
{
  "isAuthorizationEnabled": true
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|body|body|[ProductSettings](#schemaproductsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_tokens

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/tokens \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/tokens HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/tokens',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/tokens`

> Body parameter

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|body|body|[ProductToken](#schemaproducttoken)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_tokens

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/tokens \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/tokens HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/tokens',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/tokens`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "roles": [
      "Produce"
    ],
    "isActive": true,
    "expireDate": "2019-08-24T14:15:22Z",
    "description": "string",
    "issuedDate": "2019-08-24T14:15:22Z",
    "updatedDate": "2019-08-24T14:15:22Z",
    "createdDate": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "createdBy": "string"
  }
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_tokens-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ProductToken](#schemaproducttoken)]|false|none|none|
|» id|string(uuid)|false|none|none|
|» roles|[[ProductTokenRole](#schemaproducttokenrole)]¦null|false|none|none|
|» isActive|boolean|false|none|none|
|» expireDate|string(date-time)|false|none|none|
|» description|string¦null|false|none|none|
|» issuedDate|string(date-time)|false|none|none|
|» updatedDate|string(date-time)¦null|false|none|none|
|» createdDate|string(date-time)|false|none|none|
|» updatedBy|string¦null|false|none|none|
|» createdBy|string¦null|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_tokens_{key}_revoke

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/tokens/{key}/revoke`

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_tokens_{key}_revoke-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|key|path|string(uuid)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_tokens_{key}_revoke-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_tokens_{key}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/tokens/{key} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/tokens/{key} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/tokens/{key}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/tokens/{key}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/tokens/{key}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/tokens/{key}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/tokens/{key}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/tokens/{key}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/tokens/{key}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_tokens_{key}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|key|path|string(uuid)|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_tokens_{key}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[ProductToken](#schemaproducttoken)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_retentions

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/retentions \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/retentions HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/retentions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/retentions`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "name": "string",
    "type": "SOFT_TTL",
    "timeToLiveInMinutes": 0,
    "updatedDate": "2019-08-24T14:15:22Z",
    "createdDate": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "createdBy": "string"
  }
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_retentions-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ProductRetention](#schemaproductretention)]|false|none|none|
|» id|integer(int64)|false|none|none|
|» name|string¦null|false|none|none|
|» type|[RetentionType](#schemaretentiontype)|false|none|none|
|» timeToLiveInMinutes|integer(int64)|false|none|none|
|» updatedDate|string(date-time)¦null|false|none|none|
|» createdDate|string(date-time)|false|none|none|
|» updatedBy|string¦null|false|none|none|
|» createdBy|string¦null|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|type|SOFT_TTL|
|type|HARD_TTL|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_retentions

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/retentions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/retentions HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/retentions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/retentions`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|body|body|[ProductRetention](#schemaproductretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/retentions/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/retentions/{id} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/retentions/{id}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/retentions/{id}`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|id|path|integer(int64)|true|none|
|body|body|[ProductRetention](#schemaproductretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/retentions/{id} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/retentions/{id} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/retentions/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/retentions/{id}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-subscriptions">Subscriptions</h1>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|subscription|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Subscription](#schemasubscription)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}`

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|subscription|path|string|true|none|
|subscriptionType|query|[SubscriptionType](#schemasubscriptiontype)|false|none|
|subscriptionMode|query|[SubscriptionMode](#schemasubscriptionmode)|false|none|
|initialPosition|query|[InitialPosition](#schemainitialposition)|false|none|

##### Enumerated Values

|Parameter|Value|
|---|---|
|subscriptionType|Unique|
|subscriptionType|Failover|
|subscriptionType|Shared|
|subscriptionMode|Resilient|
|subscriptionMode|NonResilient|
|initialPosition|Earliest|
|initialPosition|Latest|

> Example responses

> 200 Response

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Subscription](#schemasubscription)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/subscriptions/{subscription}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|subscription|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_subscriptions_{subscription}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Subscription](#schemasubscription)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-tenants">Tenants</h1>

### get__api_v3_tenants

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants`

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}`

<h3 id="get__api_v3_tenants_{tenant}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "isActive": true,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Tenant](#schematenant)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}`

> Body parameter

```json
{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}
```

<h3 id="post__api_v3_tenants_{tenant}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|body|body|[TenantSettings](#schematenantsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_activate

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/activate \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/activate HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/activate',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/activate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/activate', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/activate', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/activate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/activate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/activate`

<h3 id="put__api_v3_tenants_{tenant}_activate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "isActive": true,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_activate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Tenant](#schematenant)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_deactivate

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/deactivate \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/deactivate HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/deactivate',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/deactivate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/deactivate', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/deactivate', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/deactivate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/deactivate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/deactivate`

<h3 id="put__api_v3_tenants_{tenant}_deactivate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "isActive": true,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_deactivate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Tenant](#schematenant)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_delete

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/delete \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/delete HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/delete',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/delete',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/delete', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/delete', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/delete");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/delete", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/delete`

<h3 id="delete__api_v3_tenants_{tenant}_delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_settings

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/settings \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/settings HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/settings',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/settings`

<h3 id="get__api_v3_tenants_{tenant}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}
```

<h3 id="get__api_v3_tenants_{tenant}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[TenantSettings](#schematenantsettings)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_settings

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/settings \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/settings HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/settings',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/settings`

> Body parameter

```json
{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}
```

<h3 id="put__api_v3_tenants_{tenant}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|body|body|[TenantSettings](#schematenantsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_tokens

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/tokens \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/tokens HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/tokens',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/tokens`

<h3 id="get__api_v3_tenants_{tenant}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_tokens-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_tokens

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/tokens \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/tokens HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "isActive": true,
  "roles": [
    "Produce"
  ],
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/tokens',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/tokens`

> Body parameter

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "isActive": true,
  "roles": [
    "Produce"
  ],
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_tokens-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|body|body|[TenantToken](#schematenanttoken)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_tokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_tokens_{key}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/tokens/{key} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/tokens/{key} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/tokens/{key}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/tokens/{key}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/tokens/{key}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/tokens/{key}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/tokens/{key}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/tokens/{key}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/tokens/{key}`

<h3 id="get__api_v3_tenants_{tenant}_tokens_{key}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|key|path|string(uuid)|true|none|

> Example responses

> 200 Response

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "isActive": true,
  "roles": [
    "Produce"
  ],
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_tokens_{key}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[TenantToken](#schematenanttoken)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_tokens_{key}_revoke

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/tokens/{key}/revoke \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/tokens/{key}/revoke HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/tokens/{key}/revoke',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/tokens/{key}/revoke',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/tokens/{key}/revoke', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/tokens/{key}/revoke', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/tokens/{key}/revoke");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/tokens/{key}/revoke", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/tokens/{key}/revoke`

<h3 id="put__api_v3_tenants_{tenant}_tokens_{key}_revoke-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|key|path|string(uuid)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_tokens_{key}_revoke-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_retentions

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/retentions \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/retentions HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/retentions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/retentions`

<h3 id="get__api_v3_tenants_{tenant}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "name": "string",
    "type": "SOFT_TTL",
    "timeToLiveInMinutes": 0,
    "updatedDate": "2019-08-24T14:15:22Z",
    "createdDate": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "createdBy": "string"
  }
]
```

<h3 id="get__api_v3_tenants_{tenant}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_retentions-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[TenantRetention](#schematenantretention)]|false|none|none|
|» id|integer(int64)|false|none|none|
|» name|string¦null|false|none|none|
|» type|[RetentionType](#schemaretentiontype)|false|none|none|
|» timeToLiveInMinutes|integer(int64)|false|none|none|
|» updatedDate|string(date-time)¦null|false|none|none|
|» createdDate|string(date-time)|false|none|none|
|» updatedBy|string¦null|false|none|none|
|» createdBy|string¦null|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|type|SOFT_TTL|
|type|HARD_TTL|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_retentions

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/retentions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/retentions HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/retentions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/retentions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/retentions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/retentions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/retentions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/retentions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/retentions`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="post__api_v3_tenants_{tenant}_retentions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|body|body|[TenantRetention](#schematenantretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_retentions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/retentions/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/retentions/{id} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/retentions/{id}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/retentions/{id}`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="put__api_v3_tenants_{tenant}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|id|path|integer(int64)|true|none|
|body|body|[TenantRetention](#schematenantretention)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_retentions_{id}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/retentions/{id} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/retentions/{id} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/retentions/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/retentions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/retentions/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/retentions/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/retentions/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/retentions/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/retentions/{id}`

<h3 id="delete__api_v3_tenants_{tenant}_retentions_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_retentions_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="andy-x-topics">Topics</h1>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|

> Example responses

> 200 Response

```json
[
  "string"
]
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[Topic](#schematopic)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}

> Code samples

```shell
## You can also use wget
curl -X POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}`

> Body parameter

```json
{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|description|query|string|false|none|
|body|body|[TopicSettings](#schematopicsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="post__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}`

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|description|query|string|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}

> Code samples

```shell
## You can also use wget
curl -X DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} \
  -H 'Accept: application/json'

```

```http
DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}`

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="delete__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings

> Code samples

```shell
## You can also use wget
curl -X GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings \
  -H 'Accept: application/json'

```

```http
GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings`

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}
```

<h3 id="get__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|[TopicSettings](#schematopicsettings)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

### put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings

> Code samples

```shell
## You can also use wget
curl -X PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v3/tenants/{tenant}/products/{product}/components/{component}/topics/{topic}/settings`

> Body parameter

```json
{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tenant|path|string|true|none|
|product|path|string|true|none|
|component|path|string|true|none|
|topic|path|string|true|none|
|body|body|[TopicSettings](#schematopicsettings)|false|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="put__api_v3_tenants_{tenant}_products_{product}_components_{component}_topics_{topic}_settings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231##section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231##section-6.5.1)|Bad Request|[ProblemDetails](#schemaproblemdetails)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235##section-3.1)|Unauthorized|[ProblemDetails](#schemaproblemdetails)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231##section-6.5.4)|Not Found|[ProblemDetails](#schemaproblemdetails)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## Schemas

<h3 id="tocS_ApplicationDetails">ApplicationDetails</h3>
<!-- backwards compatibility -->
<a id="schemaapplicationdetails"></a>
<a id="schema_ApplicationDetails"></a>
<a id="tocSapplicationdetails"></a>
<a id="tocsapplicationdetails"></a>

```json
{
  "name": "string",
  "shortName": "string",
  "version": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string¦null|false|none|none|
|shortName|string¦null|false|none|none|
|version|string¦null|false|none|none|

<h3 id="tocS_CascadeTiming">CascadeTiming</h3>
<!-- backwards compatibility -->
<a id="schemacascadetiming"></a>
<a id="schema_CascadeTiming"></a>
<a id="tocScascadetiming"></a>
<a id="tocscascadetiming"></a>

```json
"Immediate"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Immediate|
|*anonymous*|OnSaveChanges|
|*anonymous*|Never|

<h3 id="tocS_ChangeTracker">ChangeTracker</h3>
<!-- backwards compatibility -->
<a id="schemachangetracker"></a>
<a id="schema_ChangeTracker"></a>
<a id="tocSchangetracker"></a>
<a id="tocschangetracker"></a>

```json
{
  "autoDetectChangesEnabled": true,
  "lazyLoadingEnabled": true,
  "queryTrackingBehavior": "TrackAll",
  "deleteOrphansTiming": "Immediate",
  "cascadeDeleteTiming": "Immediate",
  "context": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "debugView": {
    "longView": "string",
    "shortView": "string"
  }
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|autoDetectChangesEnabled|boolean|false|none|none|
|lazyLoadingEnabled|boolean|false|none|none|
|queryTrackingBehavior|[QueryTrackingBehavior](#schemaquerytrackingbehavior)|false|none|none|
|deleteOrphansTiming|[CascadeTiming](#schemacascadetiming)|false|none|none|
|cascadeDeleteTiming|[CascadeTiming](#schemacascadetiming)|false|none|none|
|context|[DbContext](#schemadbcontext)|false|none|none|
|debugView|[DebugView](#schemadebugview)|false|none|none|

<h3 id="tocS_Cluster">Cluster</h3>
<!-- backwards compatibility -->
<a id="schemacluster"></a>
<a id="schema_Cluster"></a>
<a id="tocScluster"></a>
<a id="tocscluster"></a>

```json
{
  "inThroughputInMB": 0,
  "outThroughputInMB": 0,
  "activeDataIngestions": 0,
  "activeSubscriptions": 0,
  "name": "string",
  "shardDistributionType": "Sync",
  "status": "Online",
  "shards": [
    {
      "replicaDistributionType": "Sync",
      "replicas": [
        {
          "nodeId": "string",
          "host": "string",
          "port": "string",
          "connectionType": "SSL",
          "username": "string",
          "password": "string",
          "type": "Main",
          "isConnected": true,
          "isLocal": true,
          "x509CertificateFile": "string",
          "x509CertificatePassword": "string"
        }
      ]
    }
  ]
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|inThroughputInMB|integer(int64)|false|none|none|
|outThroughputInMB|integer(int64)|false|none|none|
|activeDataIngestions|integer(int64)|false|none|none|
|activeSubscriptions|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|shardDistributionType|[DistributionTypes](#schemadistributiontypes)|false|none|none|
|status|[ClusterStatus](#schemaclusterstatus)|false|none|none|
|shards|[[Shard](#schemashard)]¦null|false|none|none|

<h3 id="tocS_ClusterStatus">ClusterStatus</h3>
<!-- backwards compatibility -->
<a id="schemaclusterstatus"></a>
<a id="schema_ClusterStatus"></a>
<a id="tocSclusterstatus"></a>
<a id="tocsclusterstatus"></a>

```json
"Online"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Online|
|*anonymous*|PartiallyOnline|
|*anonymous*|Starting|
|*anonymous*|Offline|
|*anonymous*|Restarting|
|*anonymous*|Recovering|
|*anonymous*|Disconnecting|

<h3 id="tocS_Component">Component</h3>
<!-- backwards compatibility -->
<a id="schemacomponent"></a>
<a id="schema_Component"></a>
<a id="tocScomponent"></a>
<a id="tocscomponent"></a>

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|description|string¦null|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ComponentRetention">ComponentRetention</h3>
<!-- backwards compatibility -->
<a id="schemacomponentretention"></a>
<a id="schema_ComponentRetention"></a>
<a id="tocScomponentretention"></a>
<a id="tocscomponentretention"></a>

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|type|[RetentionType](#schemaretentiontype)|false|none|none|
|timeToLiveInMinutes|integer(int64)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ComponentSettings">ComponentSettings</h3>
<!-- backwards compatibility -->
<a id="schemacomponentsettings"></a>
<a id="schema_ComponentSettings"></a>
<a id="tocScomponentsettings"></a>
<a id="tocscomponentsettings"></a>

```json
{
  "isTopicAutomaticCreationAllowed": true,
  "enforceSchemaValidation": true,
  "isAuthorizationEnabled": true,
  "isSubscriptionAutomaticCreationAllowed": true,
  "isProducerAutomaticCreationAllowed": true
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isTopicAutomaticCreationAllowed|boolean|false|none|none|
|enforceSchemaValidation|boolean|false|none|none|
|isAuthorizationEnabled|boolean|false|none|none|
|isSubscriptionAutomaticCreationAllowed|boolean|false|none|none|
|isProducerAutomaticCreationAllowed|boolean|false|none|none|

<h3 id="tocS_ComponentToken">ComponentToken</h3>
<!-- backwards compatibility -->
<a id="schemacomponenttoken"></a>
<a id="schema_ComponentToken"></a>
<a id="tocScomponenttoken"></a>
<a id="tocscomponenttoken"></a>

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "issuedFor": "string",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|roles|[[ComponentTokenRole](#schemacomponenttokenrole)]¦null|false|none|none|
|isActive|boolean|false|none|none|
|expireDate|string(date-time)|false|none|none|
|issuedFor|string¦null|false|none|none|
|description|string¦null|false|none|none|
|issuedDate|string(date-time)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ComponentTokenRole">ComponentTokenRole</h3>
<!-- backwards compatibility -->
<a id="schemacomponenttokenrole"></a>
<a id="schema_ComponentTokenRole"></a>
<a id="tocScomponenttokenrole"></a>
<a id="tocscomponenttokenrole"></a>

```json
"Produce"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Produce|
|*anonymous*|Consume|

<h3 id="tocS_Consumer">Consumer</h3>
<!-- backwards compatibility -->
<a id="schemaconsumer"></a>
<a id="schema_Consumer"></a>
<a id="tocSconsumer"></a>
<a id="tocsconsumer"></a>

```json
{
  "subscription": "string",
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "name": "string",
  "connection": {
    "clientIpAddress": "string",
    "serverIpAddress": "string"
  },
  "connectedDate": "2019-08-24T14:15:22Z"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|subscription|string¦null|false|none|none|
|id|string(uuid)|false|none|none|
|name|string¦null|false|none|none|
|connection|[ConsumerConnection](#schemaconsumerconnection)|false|none|none|
|connectedDate|string(date-time)|false|none|none|

<h3 id="tocS_ConsumerConnection">ConsumerConnection</h3>
<!-- backwards compatibility -->
<a id="schemaconsumerconnection"></a>
<a id="schema_ConsumerConnection"></a>
<a id="tocSconsumerconnection"></a>
<a id="tocsconsumerconnection"></a>

```json
{
  "clientIpAddress": "string",
  "serverIpAddress": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|clientIpAddress|string¦null|false|none|none|
|serverIpAddress|string¦null|false|none|none|

<h3 id="tocS_DatabaseFacade">DatabaseFacade</h3>
<!-- backwards compatibility -->
<a id="schemadatabasefacade"></a>
<a id="schema_DatabaseFacade"></a>
<a id="tocSdatabasefacade"></a>
<a id="tocsdatabasefacade"></a>

```json
{
  "currentTransaction": {
    "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
    "supportsSavepoints": true
  },
  "autoTransactionsEnabled": true,
  "autoSavepointsEnabled": true,
  "providerName": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currentTransaction|[IDbContextTransaction](#schemaidbcontexttransaction)|false|none|none|
|autoTransactionsEnabled|boolean|false|none|none|
|autoSavepointsEnabled|boolean|false|none|none|
|providerName|string¦null|false|read-only|none|

<h3 id="tocS_DbContext">DbContext</h3>
<!-- backwards compatibility -->
<a id="schemadbcontext"></a>
<a id="schema_DbContext"></a>
<a id="tocSdbcontext"></a>
<a id="tocsdbcontext"></a>

```json
{
  "database": {
    "currentTransaction": {
      "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
      "supportsSavepoints": true
    },
    "autoTransactionsEnabled": true,
    "autoSavepointsEnabled": true,
    "providerName": "string"
  },
  "changeTracker": {
    "autoDetectChangesEnabled": true,
    "lazyLoadingEnabled": true,
    "queryTrackingBehavior": "TrackAll",
    "deleteOrphansTiming": "Immediate",
    "cascadeDeleteTiming": "Immediate",
    "context": {
      "database": {
        "currentTransaction": {
          "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
          "supportsSavepoints": true
        },
        "autoTransactionsEnabled": true,
        "autoSavepointsEnabled": true,
        "providerName": "string"
      },
      "changeTracker": {},
      "model": {
        "modelDependencies": {
          "typeMappingSource": {},
          "constructorBindingFactory": {},
          "parameterBindingFactories": {}
        }
      },
      "contextId": {
        "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
        "lease": 0
      }
    },
    "debugView": {
      "longView": "string",
      "shortView": "string"
    }
  },
  "model": {
    "modelDependencies": {
      "typeMappingSource": {},
      "constructorBindingFactory": {},
      "parameterBindingFactories": {}
    }
  },
  "contextId": {
    "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
    "lease": 0
  }
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|database|[DatabaseFacade](#schemadatabasefacade)|false|none|none|
|changeTracker|[ChangeTracker](#schemachangetracker)|false|none|none|
|model|[IModel](#schemaimodel)|false|none|none|
|contextId|[DbContextId](#schemadbcontextid)|false|none|none|

<h3 id="tocS_DbContextId">DbContextId</h3>
<!-- backwards compatibility -->
<a id="schemadbcontextid"></a>
<a id="schema_DbContextId"></a>
<a id="tocSdbcontextid"></a>
<a id="tocsdbcontextid"></a>

```json
{
  "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
  "lease": 0
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|instanceId|string(uuid)|false|read-only|none|
|lease|integer(int32)|false|none|none|

<h3 id="tocS_DebugView">DebugView</h3>
<!-- backwards compatibility -->
<a id="schemadebugview"></a>
<a id="schema_DebugView"></a>
<a id="tocSdebugview"></a>
<a id="tocsdebugview"></a>

```json
{
  "longView": "string",
  "shortView": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|longView|string¦null|false|read-only|none|
|shortView|string¦null|false|read-only|none|

<h3 id="tocS_DistributionTypes">DistributionTypes</h3>
<!-- backwards compatibility -->
<a id="schemadistributiontypes"></a>
<a id="schema_DistributionTypes"></a>
<a id="tocSdistributiontypes"></a>
<a id="tocsdistributiontypes"></a>

```json
"Sync"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Sync|
|*anonymous*|Async|

<h3 id="tocS_IConstructorBindingFactory">IConstructorBindingFactory</h3>
<!-- backwards compatibility -->
<a id="schemaiconstructorbindingfactory"></a>
<a id="schema_IConstructorBindingFactory"></a>
<a id="tocSiconstructorbindingfactory"></a>
<a id="tocsiconstructorbindingfactory"></a>

```json
{}

```

#### Properties

*None*

<h3 id="tocS_IDbContextTransaction">IDbContextTransaction</h3>
<!-- backwards compatibility -->
<a id="schemaidbcontexttransaction"></a>
<a id="schema_IDbContextTransaction"></a>
<a id="tocSidbcontexttransaction"></a>
<a id="tocsidbcontexttransaction"></a>

```json
{
  "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
  "supportsSavepoints": true
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|transactionId|string(uuid)|false|read-only|none|
|supportsSavepoints|boolean|false|read-only|none|

<h3 id="tocS_IModel">IModel</h3>
<!-- backwards compatibility -->
<a id="schemaimodel"></a>
<a id="schema_IModel"></a>
<a id="tocSimodel"></a>
<a id="tocsimodel"></a>

```json
{
  "modelDependencies": {
    "typeMappingSource": {},
    "constructorBindingFactory": {},
    "parameterBindingFactories": {}
  }
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|modelDependencies|[RuntimeModelDependencies](#schemaruntimemodeldependencies)|false|none|none|

<h3 id="tocS_IParameterBindingFactories">IParameterBindingFactories</h3>
<!-- backwards compatibility -->
<a id="schemaiparameterbindingfactories"></a>
<a id="schema_IParameterBindingFactories"></a>
<a id="tocSiparameterbindingfactories"></a>
<a id="tocsiparameterbindingfactories"></a>

```json
{}

```

#### Properties

*None*

<h3 id="tocS_ITypeMappingSource">ITypeMappingSource</h3>
<!-- backwards compatibility -->
<a id="schemaitypemappingsource"></a>
<a id="schema_ITypeMappingSource"></a>
<a id="tocSitypemappingsource"></a>
<a id="tocsitypemappingsource"></a>

```json
{}

```

#### Properties

*None*

<h3 id="tocS_InitialPosition">InitialPosition</h3>
<!-- backwards compatibility -->
<a id="schemainitialposition"></a>
<a id="schema_InitialPosition"></a>
<a id="tocSinitialposition"></a>
<a id="tocsinitialposition"></a>

```json
"Earliest"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Earliest|
|*anonymous*|Latest|

<h3 id="tocS_NodeConnectionType">NodeConnectionType</h3>
<!-- backwards compatibility -->
<a id="schemanodeconnectiontype"></a>
<a id="schema_NodeConnectionType"></a>
<a id="tocSnodeconnectiontype"></a>
<a id="tocsnodeconnectiontype"></a>

```json
"SSL"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|SSL|
|*anonymous*|NON_SSL|

<h3 id="tocS_ProblemDetails">ProblemDetails</h3>
<!-- backwards compatibility -->
<a id="schemaproblemdetails"></a>
<a id="schema_ProblemDetails"></a>
<a id="tocSproblemdetails"></a>
<a id="tocsproblemdetails"></a>

```json
{
  "type": "string",
  "title": "string",
  "status": 0,
  "detail": "string",
  "instance": "string",
  "property1": null,
  "property2": null
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|**additionalProperties**|any|false|none|none|
|type|string¦null|false|none|none|
|title|string¦null|false|none|none|
|status|integer(int32)¦null|false|none|none|
|detail|string¦null|false|none|none|
|instance|string¦null|false|none|none|

<h3 id="tocS_Producer">Producer</h3>
<!-- backwards compatibility -->
<a id="schemaproducer"></a>
<a id="schema_Producer"></a>
<a id="tocSproducer"></a>
<a id="tocsproducer"></a>

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "instanceType": "Single",
  "publicIpRange": [
    "string"
  ],
  "privateIpRange": [
    "string"
  ],
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|description|string¦null|false|none|none|
|instanceType|[ProducerInstanceType](#schemaproducerinstancetype)|false|none|none|
|publicIpRange|[string]¦null|false|none|none|
|privateIpRange|[string]¦null|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ProducerActivity">ProducerActivity</h3>
<!-- backwards compatibility -->
<a id="schemaproduceractivity"></a>
<a id="schema_ProducerActivity"></a>
<a id="tocSproduceractivity"></a>
<a id="tocsproduceractivity"></a>

```json
{
  "key": "string",
  "tenant": "string",
  "name": "string",
  "location": "string",
  "isActive": true,
  "instancesCount": 0
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string¦null|false|none|none|
|tenant|string¦null|false|none|none|
|name|string¦null|false|none|none|
|location|string¦null|false|none|none|
|isActive|boolean|false|none|none|
|instancesCount|integer(int32)|false|none|none|

<h3 id="tocS_ProducerInstanceType">ProducerInstanceType</h3>
<!-- backwards compatibility -->
<a id="schemaproducerinstancetype"></a>
<a id="schema_ProducerInstanceType"></a>
<a id="tocSproducerinstancetype"></a>
<a id="tocsproducerinstancetype"></a>

```json
"Single"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Single|
|*anonymous*|Multiple|

<h3 id="tocS_Product">Product</h3>
<!-- backwards compatibility -->
<a id="schemaproduct"></a>
<a id="schema_Product"></a>
<a id="tocSproduct"></a>
<a id="tocsproduct"></a>

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|description|string¦null|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ProductRetention">ProductRetention</h3>
<!-- backwards compatibility -->
<a id="schemaproductretention"></a>
<a id="schema_ProductRetention"></a>
<a id="tocSproductretention"></a>
<a id="tocsproductretention"></a>

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|type|[RetentionType](#schemaretentiontype)|false|none|none|
|timeToLiveInMinutes|integer(int64)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ProductSettings">ProductSettings</h3>
<!-- backwards compatibility -->
<a id="schemaproductsettings"></a>
<a id="schema_ProductSettings"></a>
<a id="tocSproductsettings"></a>
<a id="tocsproductsettings"></a>

```json
{
  "isAuthorizationEnabled": true
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isAuthorizationEnabled|boolean|false|none|none|

<h3 id="tocS_ProductToken">ProductToken</h3>
<!-- backwards compatibility -->
<a id="schemaproducttoken"></a>
<a id="schema_ProductToken"></a>
<a id="tocSproducttoken"></a>
<a id="tocsproducttoken"></a>

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "roles": [
    "Produce"
  ],
  "isActive": true,
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|roles|[[ProductTokenRole](#schemaproducttokenrole)]¦null|false|none|none|
|isActive|boolean|false|none|none|
|expireDate|string(date-time)|false|none|none|
|description|string¦null|false|none|none|
|issuedDate|string(date-time)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_ProductTokenRole">ProductTokenRole</h3>
<!-- backwards compatibility -->
<a id="schemaproducttokenrole"></a>
<a id="schema_ProductTokenRole"></a>
<a id="tocSproducttokenrole"></a>
<a id="tocsproducttokenrole"></a>

```json
"Produce"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Produce|
|*anonymous*|Consume|

<h3 id="tocS_QueryTrackingBehavior">QueryTrackingBehavior</h3>
<!-- backwards compatibility -->
<a id="schemaquerytrackingbehavior"></a>
<a id="schema_QueryTrackingBehavior"></a>
<a id="tocSquerytrackingbehavior"></a>
<a id="tocsquerytrackingbehavior"></a>

```json
"TrackAll"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|TrackAll|
|*anonymous*|NoTracking|
|*anonymous*|NoTrackingWithIdentityResolution|

<h3 id="tocS_Replica">Replica</h3>
<!-- backwards compatibility -->
<a id="schemareplica"></a>
<a id="schema_Replica"></a>
<a id="tocSreplica"></a>
<a id="tocsreplica"></a>

```json
{
  "nodeId": "string",
  "host": "string",
  "port": "string",
  "connectionType": "SSL",
  "username": "string",
  "password": "string",
  "type": "Main",
  "isConnected": true,
  "isLocal": true,
  "x509CertificateFile": "string",
  "x509CertificatePassword": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|nodeId|string¦null|false|none|none|
|host|string¦null|false|none|none|
|port|string¦null|false|none|none|
|connectionType|[NodeConnectionType](#schemanodeconnectiontype)|false|none|none|
|username|string¦null|false|none|none|
|password|string¦null|false|none|none|
|type|[ReplicaTypes](#schemareplicatypes)|false|none|none|
|isConnected|boolean|false|none|none|
|isLocal|boolean|false|none|none|
|x509CertificateFile|string¦null|false|none|none|
|x509CertificatePassword|string¦null|false|none|none|

<h3 id="tocS_ReplicaTypes">ReplicaTypes</h3>
<!-- backwards compatibility -->
<a id="schemareplicatypes"></a>
<a id="schema_ReplicaTypes"></a>
<a id="tocSreplicatypes"></a>
<a id="tocsreplicatypes"></a>

```json
"Main"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Main|
|*anonymous*|Worker|
|*anonymous*|BackupReplica|

<h3 id="tocS_RetentionType">RetentionType</h3>
<!-- backwards compatibility -->
<a id="schemaretentiontype"></a>
<a id="schema_RetentionType"></a>
<a id="tocSretentiontype"></a>
<a id="tocsretentiontype"></a>

```json
"SOFT_TTL"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|SOFT_TTL|
|*anonymous*|HARD_TTL|

<h3 id="tocS_RuntimeModelDependencies">RuntimeModelDependencies</h3>
<!-- backwards compatibility -->
<a id="schemaruntimemodeldependencies"></a>
<a id="schema_RuntimeModelDependencies"></a>
<a id="tocSruntimemodeldependencies"></a>
<a id="tocsruntimemodeldependencies"></a>

```json
{
  "typeMappingSource": {},
  "constructorBindingFactory": {},
  "parameterBindingFactories": {}
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|typeMappingSource|[ITypeMappingSource](#schemaitypemappingsource)|false|none|none|
|constructorBindingFactory|[IConstructorBindingFactory](#schemaiconstructorbindingfactory)|false|none|none|
|parameterBindingFactories|[IParameterBindingFactories](#schemaiparameterbindingfactories)|false|none|none|

<h3 id="tocS_Shard">Shard</h3>
<!-- backwards compatibility -->
<a id="schemashard"></a>
<a id="schema_Shard"></a>
<a id="tocSshard"></a>
<a id="tocsshard"></a>

```json
{
  "replicaDistributionType": "Sync",
  "replicas": [
    {
      "nodeId": "string",
      "host": "string",
      "port": "string",
      "connectionType": "SSL",
      "username": "string",
      "password": "string",
      "type": "Main",
      "isConnected": true,
      "isLocal": true,
      "x509CertificateFile": "string",
      "x509CertificatePassword": "string"
    }
  ]
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|replicaDistributionType|[DistributionTypes](#schemadistributiontypes)|false|none|none|
|replicas|[[Replica](#schemareplica)]¦null|false|none|none|

<h3 id="tocS_Subscription">Subscription</h3>
<!-- backwards compatibility -->
<a id="schemasubscription"></a>
<a id="schema_Subscription"></a>
<a id="tocSsubscription"></a>
<a id="tocssubscription"></a>

```json
{
  "tenant": "string",
  "product": "string",
  "component": "string",
  "topic": "string",
  "subscriptionName": "string",
  "subscriptionType": "Unique",
  "subscriptionMode": "Resilient",
  "initialPosition": "Earliest",
  "consumersConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "consumerExternalConnected": {
    "property1": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    },
    "property2": {
      "subscription": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "connection": {
        "clientIpAddress": "string",
        "serverIpAddress": "string"
      },
      "connectedDate": "2019-08-24T14:15:22Z"
    }
  },
  "currentConnectionIndex": 0,
  "subscriptionPositionContext": {
    "database": {
      "currentTransaction": {
        "transactionId": "75906707-8c31-479c-b354-aa805c4cefbc",
        "supportsSavepoints": true
      },
      "autoTransactionsEnabled": true,
      "autoSavepointsEnabled": true,
      "providerName": "string"
    },
    "changeTracker": {
      "autoDetectChangesEnabled": true,
      "lazyLoadingEnabled": true,
      "queryTrackingBehavior": "TrackAll",
      "deleteOrphansTiming": "Immediate",
      "cascadeDeleteTiming": "Immediate",
      "context": {},
      "debugView": {
        "longView": "string",
        "shortView": "string"
      }
    },
    "model": {
      "modelDependencies": {
        "typeMappingSource": {},
        "constructorBindingFactory": {},
        "parameterBindingFactories": {}
      }
    },
    "contextId": {
      "instanceId": "64d2028c-ae87-4069-a624-66089d957ef9",
      "lease": 0
    }
  },
  "createdDate": "2019-08-24T14:15:22Z"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tenant|string¦null|false|none|none|
|product|string¦null|false|none|none|
|component|string¦null|false|none|none|
|topic|string¦null|false|none|none|
|subscriptionName|string¦null|false|none|none|
|subscriptionType|[SubscriptionType](#schemasubscriptiontype)|false|none|none|
|subscriptionMode|[SubscriptionMode](#schemasubscriptionmode)|false|none|none|
|initialPosition|[InitialPosition](#schemainitialposition)|false|none|none|
|consumersConnected|object¦null|false|none|none|
|» **additionalProperties**|[Consumer](#schemaconsumer)|false|none|none|
|consumerExternalConnected|object¦null|false|none|none|
|» **additionalProperties**|[Consumer](#schemaconsumer)|false|none|none|
|currentConnectionIndex|integer(int32)|false|none|none|
|subscriptionPositionContext|[DbContext](#schemadbcontext)|false|none|none|
|createdDate|string(date-time)|false|none|none|

<h3 id="tocS_SubscriptionActivity">SubscriptionActivity</h3>
<!-- backwards compatibility -->
<a id="schemasubscriptionactivity"></a>
<a id="schema_SubscriptionActivity"></a>
<a id="tocSsubscriptionactivity"></a>
<a id="tocssubscriptionactivity"></a>

```json
{
  "name": "string",
  "location": "string",
  "isActive": true
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string¦null|false|none|none|
|location|string¦null|false|none|none|
|isActive|boolean|false|none|none|

<h3 id="tocS_SubscriptionMode">SubscriptionMode</h3>
<!-- backwards compatibility -->
<a id="schemasubscriptionmode"></a>
<a id="schema_SubscriptionMode"></a>
<a id="tocSsubscriptionmode"></a>
<a id="tocssubscriptionmode"></a>

```json
"Resilient"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Resilient|
|*anonymous*|NonResilient|

<h3 id="tocS_SubscriptionType">SubscriptionType</h3>
<!-- backwards compatibility -->
<a id="schemasubscriptiontype"></a>
<a id="schema_SubscriptionType"></a>
<a id="tocSsubscriptiontype"></a>
<a id="tocssubscriptiontype"></a>

```json
"Unique"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Unique|
|*anonymous*|Failover|
|*anonymous*|Shared|

<h3 id="tocS_Tenant">Tenant</h3>
<!-- backwards compatibility -->
<a id="schematenant"></a>
<a id="schema_Tenant"></a>
<a id="tocStenant"></a>
<a id="tocstenant"></a>

```json
{
  "id": 0,
  "name": "string",
  "isActive": true,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|isActive|boolean|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_TenantRetention">TenantRetention</h3>
<!-- backwards compatibility -->
<a id="schematenantretention"></a>
<a id="schema_TenantRetention"></a>
<a id="tocStenantretention"></a>
<a id="tocstenantretention"></a>

```json
{
  "id": 0,
  "name": "string",
  "type": "SOFT_TTL",
  "timeToLiveInMinutes": 0,
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|type|[RetentionType](#schemaretentiontype)|false|none|none|
|timeToLiveInMinutes|integer(int64)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_TenantSettings">TenantSettings</h3>
<!-- backwards compatibility -->
<a id="schematenantsettings"></a>
<a id="schema_TenantSettings"></a>
<a id="tocStenantsettings"></a>
<a id="tocstenantsettings"></a>

```json
{
  "isProductAutomaticCreationAllowed": true,
  "isEncryptionEnabled": true,
  "isAuthorizationEnabled": true
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isProductAutomaticCreationAllowed|boolean|false|none|none|
|isEncryptionEnabled|boolean|false|none|none|
|isAuthorizationEnabled|boolean|false|none|none|

<h3 id="tocS_TenantToken">TenantToken</h3>
<!-- backwards compatibility -->
<a id="schematenanttoken"></a>
<a id="schema_TenantToken"></a>
<a id="tocStenanttoken"></a>
<a id="tocstenanttoken"></a>

```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "isActive": true,
  "roles": [
    "Produce"
  ],
  "expireDate": "2019-08-24T14:15:22Z",
  "description": "string",
  "issuedDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|isActive|boolean|false|none|none|
|roles|[[TenantTokenRole](#schematenanttokenrole)]¦null|false|none|none|
|expireDate|string(date-time)|false|none|none|
|description|string¦null|false|none|none|
|issuedDate|string(date-time)|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_TenantTokenRole">TenantTokenRole</h3>
<!-- backwards compatibility -->
<a id="schematenanttokenrole"></a>
<a id="schema_TenantTokenRole"></a>
<a id="tocStenanttokenrole"></a>
<a id="tocstenanttokenrole"></a>

```json
"Produce"

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

##### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|Produce|
|*anonymous*|Consume|

<h3 id="tocS_Topic">Topic</h3>
<!-- backwards compatibility -->
<a id="schematopic"></a>
<a id="schema_Topic"></a>
<a id="tocStopic"></a>
<a id="tocstopic"></a>

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "createdBy": "string"
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string¦null|false|none|none|
|description|string¦null|false|none|none|
|updatedDate|string(date-time)¦null|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedBy|string¦null|false|none|none|
|createdBy|string¦null|false|none|none|

<h3 id="tocS_TopicSettings">TopicSettings</h3>
<!-- backwards compatibility -->
<a id="schematopicsettings"></a>
<a id="schema_TopicSettings"></a>
<a id="tocStopicsettings"></a>
<a id="tocstopicsettings"></a>

```json
{
  "writeBufferSizeInBytes": 0,
  "maxWriteBufferNumber": 0,
  "maxWriteBufferSizeToMaintain": 0,
  "minWriteBufferNumberToMerge": 0,
  "maxBackgroundCompactionsThreads": 0,
  "maxBackgroundFlushesThreads": 0
}

```

#### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|writeBufferSizeInBytes|integer(int64)|false|none|none|
|maxWriteBufferNumber|integer(int32)|false|none|none|
|maxWriteBufferSizeToMaintain|integer(int32)|false|none|none|
|minWriteBufferNumberToMerge|integer(int32)|false|none|none|
|maxBackgroundCompactionsThreads|integer(int32)|false|none|none|
|maxBackgroundFlushesThreads|integer(int32)|false|none|none|

