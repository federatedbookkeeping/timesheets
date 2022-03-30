## Create an Entry

```
POST /v2/entries

```

### Input

date

_Required_  **string**  of a date in ISO 8061 format  `YYYY-MM-DD`

The date of the time entry.

user_id

_Optional_  **integer**

The ID of the user who logged this time entry. If no value is provided, the authenticated user will be used.

minutes

_Required_  **integer**

The number of minutes logged in this time entry. This number will automatically be rounded up based on the project’s “billing_increment” settings.

description

_Optional_  **string**

The description of the time entry. Any tags or hashtags will be automatically parsed.

project_id

_Optional_  **integer**

The ID of the project this time entry is logged under. If no value is provided, this time entry will not be logged under any project.

project_name

_Optional_  **string**

The name of the project this time entry is logged under. If no value is provided, this time entry will not be logged under any project.

This value is only used if no value is provided for  `project_id`.

If a project with this name does not exist yet, it will automatically be created with this entry.

source_url

_Optional_  **string**

A URL that corresponds to the work completed in this time entry. Some Examples Include:

-   the URL to a commit in a version control platform like  [Github or Beanstalk](http://help.nokotime.com/article/74-log-time-from-github)

-   the URL to a specific task in a project management app like  [Planscope](https://planscope.io/)  or  [Basecamp](https://planscope.io/)

-   the URL to a client’s website.

```javascript
{
  "date": "2012-01-09",
  "user_id": 5538,
  "minutes": 60,
  "description": "noko",
  "project_id": 37396,
  "project_name": "Gear GmbH",
  "source_url": "http://someapp.com/special/url/"
}
```

### Reponse

```
Status: 201 Created
Location: https://api.nokotime.com/v2/entries/1
```

```javascript
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
```
