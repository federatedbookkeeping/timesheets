
## List Entries

Get all entries, sorted by the most recent entry date.

```
GET /v2/entries

```

### Parameters

Each parameter passed will filter the results, and parameters are chained (meaning that if you search by  `users`  and  `projects`, it will only return entries from those users for those projects).

user_ids

_Optional_  **string**

A comma-separated list of user IDs to filter by.

Example:  `user_ids=1,2,3`

description

_Optional_  **string**

Only entries containing this text in their description are returned.

Example:  `description=meeting`

project_ids

_Optional_  **string**

A comma-separated list of project IDs to filter by.

Example:  `project_ids=4,5,6`

tag_ids

_Optional_  **string**

A comma-separated list of tag IDs to filter by.

Example:  `tag_ids=7,8,9`

tag_filter_type

_Optional_  **string**

Indicates how to filter by tags.

Accepted values:  `and`  (**default**),  `combination of`

invoice_ids

_Optional_  **string**

A comma-separated list of invoice IDs to filter by.

Example:  `invoice_ids=1,2,3`

import_ids

_Optional_  **string**

A comma-separated list of import IDs to filter by.

Example:  `import_ids=4,5,6`

from

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries from or after this date will be returned.

Example:  `from=2013-09-27`

to

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries on or before this date will be returned.

Example:  `to=2013-09-27`

invoiced

_Optional_  **boolean**

`true`: only show invoiced entries

`false`: only shows uninvoiced entries

invoiced_at_from

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries invoiced from or after this date will be returned.

Example:  `invoiced_at_from=2013-09-27`

invoiced_at_to

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries invoiced on or before this date will be returned.

Example:  `invoiced_at_to=2013-09-27`

updated_from

_Optional_  **string**  of a timestamp in ISO 8061 format  `YYYY-MM-DDTHH:MM:SSZ`

Only entries updated from or after this timestamp will be returned.

Example:  `updated_from=2012-01-09T08:33:29Z`

updated_to

_Optional_  **string**  of a timestamp in ISO 8061 format  `YYYY-MM-DDTHH:MM:SSZ`

Only entries updated on or before this timestamp will be returned.

Example:  `updated_to=2012-01-09T08:33:29Z`

billable

_Optional_  **boolean**

`true`: only show billable entries

`false`: only shows unbillable entries

approved_at_from

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries approved from or after this date will be returned.

Example:  `approved_at_from=2013-09-27`

approved_at_to

_Optional_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

Only entries approved on or before this date will be returned.

Example:  `approved_at_to=2013-09-27`

approved_by_ids

_Optional_  **string**

A comma-separated list of user IDs to filter by.

Only entries that have been approved by these users will be returned.

Example:  `approved_by_ids=1,2,3`

### Response

```
Status: 200 OK
Link: <https://api.nokotime.com/v2/entries?page=2>; rel="next",
 <https://api.nokotime.com/v2/entries?page=5>; rel="last"
```

```javascript
[
  {
    "id": 1,
    "date": "2012-01-09",
    "user": {
      "id": 5538,
      "email": "john.test@test.com",
      "first_name": "John",
      "last_name": "Test",
      "profile_image_url": "https://api.nokotime.com/images/avatars/0000/0001/avatar.jpg",
      "url": "https://api.nokotime.com/v2/users/5538"
    },
    "billable": true,
    "minutes": 60,
    "description": "noko",
    "project": {
      "id": 37396,
      "name": "Gear GmbH",
      "billing_increment": 10,
      "enabled": true,
      "billable": true,
      "color": "#ff9898",
      "url": "https://api.nokotime.com/v2/projects/37396"
    },
    "tags": [
      {
        "id": 249397,
        "name": "noko",
        "billable": true,
        "formatted_name": "#noko",
        "url": "https://api.nokotime.com/v2/tags/249397"
      }
    ],
    "source_url": "http://someapp.com/special/url/",
    "invoiced_at": "2012-01-10T08:33:29Z",
    "invoice": {
      "id": 12345678,
      "reference": "AA001",
      "invoice_date": "2013-07-09",
      "state": "unpaid",
      "total_amount": 189.33,
      "url": "https://api.nokotime.com/v2/invoices/12345678"
    },
    "import": {
      "id": 8910,
      "url": "https://api.nokotime.com/v2/imports/8910"
    },
    "approved_at": "2012-01-10T08:33:29Z",
    "approved_by": {
      "id": 5538,
      "email": "john.test@test.com",
      "first_name": "John",
      "last_name": "Test",
      "profile_image_url": "https://api.nokotime.com/images/avatars/0000/0001/avatar.jpg",
      "url": "https://api.nokotime.com/v2/users/5538"
    },
    "url": "https://api.nokotime.com/v2/entries/1711626",
    "invoiced_outside_of_noko_url": "https://api.nokotime.com/v2/entries/1711626/marked_as_invoiced",
    "approved_url": "https://api.nokotime.com/v2/entries/1711626/approved",
    "unapproved_url": "https://api.nokotime.com/v2/entries/1711626/unapproved",
    "created_at": "2012-01-09T08:33:29Z",
    "updated_at": "2012-01-09T08:33:29Z"
  }
]
```
