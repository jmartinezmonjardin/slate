# Xchool REST API

Welcome to the XCHOOL REST API! You can use our API to access XCHOOL endpoints, which can give you information about courses, users and progress from our database.

You can see code samples in the dark area on the right.

# Authentication

To use XCHOOL REST API endpoints, you will have to add two parameters in each call to authenticate.

Parameter | Type | Required | Description |
--------- | ---- | ----------| ----------- |
timestamp | Integer | Yes | Actual date time in seconds from 1970/01/01 (Unix timestamp)
signature | String | Yes | Security signature

## How to create signature

```bash
timestamp=$(date +%s)
user_token="k5zQW_uE"
api_secret_key="zC-bGbSjMyVdzTuC"

string="$user_token$timestamp$api_secret_key"

echo -n $string | openssl dgst -sha1
```

The <code>signature</code> param is a string encrypted using the SHA-1 algorithm. The string is calculated as <code>string = user_token + timestamp + api_secret_key
</code>. When:

String | Description |
------ | ----------- |
user_token | Identifier to get user in API endpoints. The user must have sufficient permissions to perform the specific action.
timestamp | <code>timestamp</code> value param.
api_secret_key | Uniq secret key. Provided by XTEACH.




# Errores
La API de XCHOOL utiliza los siguientes errores comununes:


Estado | Código de error | Meaning |
------ | --------------- | ------- |
400 | - | Bad Request -- La petición es inválida.
401 | 1 | Unauthorized -- La Xchool no tiene asignada un Api Consumer. Póngase en contacto con el administrador.
401 | 2 | Unauthorized -- Error en la autenticación.
401 | 7 | Unauthorized -- La petición ha expirado.
404 | 3 | User Not Found -- No se ha encontrado ningún usuario con el <code>user_token</code> indicado.
404 | 4 | Course Not Found -- No se ha encontrado el curso indicado.
404 | 5 | Lesson Not Found -- No se ha encontrado el módulo indicado.
404 | 6 | Xchool Not Found -- No se ha encontrado la Xchool indicada.
405 | - | Method Not Allowed -- You tried to access a kitten with an invalid method.
406 | - | Not Acceptable -- You requested a format that isn't json.
500 | - | Internal Server Error -- Tenemos un problema con nuestro servidor. Inténtelo más tarde.
503 | - | Service Unavailable -- Temporalmente fuera de servicio. Inténtelo más tarde.

<!-- # Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside> -->
