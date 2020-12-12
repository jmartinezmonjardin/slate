# Users
## The User object
```shell
{
  "user_id": 1234,
  "user_token": "yNb6bptb",
  "slug": "user-1234",
  "email": "user-1234@localhost.com",
  "name": "User",
  "surname": "1234",
  "birthdate": '1987-05-29',
  "gender": 'female',
  "country": 'Spain',
  "state": 'Asturias',
  "city": 'Gijón',
  "company": 'Xteach',
  "job": 'Developer',
  "tagline": 'Spread Your Knowledege',
  "phone": '985000000',
  "inscription_school_id": 123,
  "id_card": '11111111H',
  "created_at": "2020-08-27T09:10:04.000+02:00",
  "updated_at": "2020-08-27T09:10:35.000+02:00",
  "enrollments_count": 1,
  "enrollments": [
    {
        "id": 1234,
        "course_id": 123,
        "last_access_at": "2020-08-28T11:10:35.000+02:00",
        "last_page": 1234,
        "time": 12345,
        "complete": true,
        "evaluation": 70.0,
        "active": true,
        "graduate": true,
        "graduated_at": "2020-08-28T11:10:35.000+02:00",
        "progress": 100.0,
        "time_study": 1234,
        "last_activity_at": "2020-08-28T11:10:35.000+02:00",
        "created_at": "2020-08-27T09:10:35.000+02:00",
        "updated_at": "2020-08-27T09:10:35.000+02:00"
    }
  ]
}
```

Attribute | Type | Description |
--------- | ---- | ----------- |
user_id | Integer | A unique identifier for the resource.
user_token | String | Identifier to get user in API endpoints.
slug | String | A unique identifier for the resource.
email | String | The user email.
name | String | The user name.
surname | String | The user surname.
birthdate | String | The user birthdate in an ISO 8601 format of YYYY-MM-DD.
gender | String | The user gender. One of <code>male</code> and <code>female</code>.
country | String | The user Country.
state | String | The user State.
city | String | The user City.
company | String | The user Company.
job | String | The user job.
tagline | String | Short introduction to the biography of user.
phone | String | The user number phone.
inscription_school_id | Integer | Identifier of XCHOOL from which the user was created.
id_card | String | The user Id card number.
created_at | String | The user creation date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
updated_at | String | The user update date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
enrollments_cout | Integer | Number of courses enrollments of user
enrollments | Array | An array of [Enrollment](/#enrollment) objects

### Enrollment
Attribute | Type | Description |
--------- | ---- | ----------- |
id | Integer | A unique identifier for the resource.
course_id | Integer | Identifier of [Course](/#course) object in which user are enrolled.
last_access_at | String | The last access course date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
last_page | Integer | Identifier of last [Lesson](/#lesson) object that user accessed.
time | Integer |
complete | Boolean | Indicates if the user completed the course.
evaluation | Float | User course score.
active | Boolean |
graduate | Boolean | Indicates if the user has graduated from the course.
graduated_at | String | The graduate date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
progress | Float | User course progress.
time_study | Integer | Studying time in seconds.
last_activity_at | String | The last activity date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
created_at | String | The user creation date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.
updated_at | String | The user update date time in an ISO 8601 format of YYYY-MM-DDTHH:MM:SS.

## List users
```bash
curl -X GET "https://sgs.xchool.es/api/sgs/users.json" \
     -d timestamp=1601291526 \
     -d signature=3d9e1079c729bccf1fb71f60ee81a8d0d98645a3


{
  "success": true,
  "users_count": 2,
  "users": [
    {
      "user_id": 1234,
      "user_token": "yNb6bptb",
      "slug": "user-1234",
      "email": "user-1234@localhost.com",
      "name": "User",
      "surname": "1234",
      "birthdate": '1987-05-29',
      "gender": 'female',
      "country": 'Spain',
      "state": 'Asturias',
      "city": 'Gijón',
      "company": 'Xteach',
      "job": 'Developer',
      "tagline": 'Spread Your Knowledege',
      "phone": '985000000',
      "inscription_school_id": 123,
      "id_card": '11111111H',
      "created_at": "2020-08-27T09:10:04.000+02:00",
      "updated_at": "2020-08-27T09:10:35.000+02:00",
      "enrollments_count": 1,
      "enrollments": [
        {
            "id": 1234,
            "course_id": 123,
            "last_access_at": "2020-08-28T11:10:35.000+02:00",
            "last_page": 1234,
            "time": 12345,
            "complete": true,
            "evaluation": 70.0,
            "active": true,
            "graduate": true,
            "graduated_at": "2020-08-28T11:10:35.000+02:00",
            "progress": 100.0,
            "time_study": 1234,
            "last_activity_at": "2020-08-28T11:10:35.000+02:00",
            "created_at": "2020-08-27T09:10:35.000+02:00",
            "updated_at": "2020-08-27T09:10:35.000+02:00"
        }
      ]
    },
    {
      "user_id": 1456,
      "user_token": "yNb6bptb",
      "slug": "user-1456",
      "email": "user-1456@localhost.com",
      "name": "User",
      "surname": "1456",
      "birthdate": '1987-05-29',
      "gender": 'female',
      "country": 'Spain',
      "state": 'Asturias',
      "city": 'Gijón',
      "company": 'Xteach',
      "job": 'Developer',
      "tagline": 'Spread Your Knowledege',
      "phone": '985000000',
      "inscription_school_id": 123,
      "id_card": '11111111H',
      "created_at": "2020-08-27T09:10:04.000+02:00",
      "updated_at": "2020-08-27T09:10:35.000+02:00",
      "enrollments_count": 1,
      "enrollments": [
        {
            "id": 1456,
            "course_id": 123,
            "last_access_at": "2020-08-28T11:10:35.000+02:00",
            "last_page": 1456,
            "time": 14561,
            "complete": true,
            "evaluation": 30.0,
            "active": true,
            "graduate": false,
            "graduated_at": "2020-08-28T11:10:35.000+02:00",
            "progress": 100.0,
            "time_study": 1223,
            "last_activity_at": "2020-08-28T11:10:35.000+02:00",
            "created_at": "2020-08-27T09:10:35.000+02:00",
            "updated_at": "2020-08-27T09:10:35.000+02:00"
        }
      ]
    }
  ]
}
```
<code>GET /api/v3/users?timestamp={timestamp}&signature={signature}</code>

### Parameters list

Parameter | Description | Required |
--------- | ----------- | -------- |
timestamp | Actual date time in seconds from 1970/01/01 (Unix timestamp) | Yes
signatured | Security signature | Yes
user_ids | List of user identifiers, separated by commas. E. g. <code>user_ids=1,2,3,4</code> | No
course_ids | List of course identifiers, separated by commas. E. g. <code>course_ids=8,9,10</code> | No
limit_by_school | Defaults to <code>false</code>. If <code>true</code>, return only users from XCHOOL defined by subdomain; if <code>false</code>, return users from all user's XCHOOLS | No

### Response attributes
Attribute | Type | Description |
--------- | ---- | ----------- |
success | Boolean | Indicates whether the operation has completed successfully or an error has occurred
users_count | Integer | Total number of users
users | Array | An array of [User](/#the-user-object) objects

## Create new user

## Retrieve a particular user


# Cursos
## The course object

## List courses

## Retrieve a particular course


# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
