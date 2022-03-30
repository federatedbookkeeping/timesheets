## [Veryfi API](veryfi.com)

You need sign up first after it they have documentation for working with API.

`POST` Submit a request to process a multipart/form-data file upload.

```

curl -H "Content-Type: multipart/form-data" \
     -H "Accept: application/json" \
     -H "CLIENT-ID: CLIENT_ID" \
     -H "AUTHORIZATION: apikey USERNAME:API_KEY" \
     -X POST \
     -F 'file=@/Users/admin/tmp/panera_receipt.pdf' \
     -F 'file_name=panera_receipt.pdf' \
     https://api.veryfi.com/api/v7/partner/documents/
```     
response
```json
{
    "id": 12345678,
    "img_url": "https://cdn.veryfi.com/receipts/c45f9514-0c48-4f49-9005-f5e5b39da401.jpg",
    "img_thumbnail_url": "https://cdn.veryfi.com/receipts/c45f9514-0c48-f5e5b39da401_t.jpg",
    "card_number": "4037",
    "category": "Meals & Entertainment", 
    "currency_code": "USD",
    "date": "2018-06-23 19:56:00", 
    "payment_type": "",
    "phone_number": "8183911059", 
    "subtotal": 50.68,
    "tax": 10.00,
    "tip": 0.0,
    "total": 60.68,
    "vendor": {
        "address": "132 Palm Ave, Burbank, CA 91502, USA",
        "name": "Panera Bread",
        "vendor_logo": "https://cdn.veryfi.com/logos/us/910164080.png", 
        "vendor_type": "cafe"
    },
}
```

`GET` Retrieve previously processed documents.

```
curl    -H "Content-Type: application/json" \
        -H "Accept: application/json" \
        -H "CLIENT-ID: CLIENT_ID" \
        -H "AUTHORIZATION: apikey USERNAME:API_KEY" \
        -X GET https://api.veryfi.com/api/v7/partner/documents/?q=keyword&created__gte=2020-07-01+00:00:00
```

response
```json

    {
        "id": 26566742, 
        "img_url": "https://scdn.veryfi.com/receipts/c45f9514-0c48-4f49-9005-f5ddd9da555.jpg",
        "img_thumbnail_url": "https://scdn.veryfi.com/receipts/c45f9514-0c48-f5ddd9da555_t.jpg",
        "card_number": "4037",
        "category": "Meals & Entertainment",
        "currency_code": "USD",
        "date": "2018-06-21 12:32:00",
        "payment_type": "",
        "phone_number": "8183911059",
        "subtotal": 25.34,
        "tax": 5.00,
        "tip": 0.0,
        "total": 30.34,
        "vendor": {
            "address": "132 Palm Ave, Burbank, CA 91502, USA",
            "name": "Panera Bread",
            "vendor_logo": "https://cdn.veryfi.com/logos/us/910164080.png",
            "vendor_type": "cafe"
        },

        ...
    },
    {
        "id": 26566743, 
        "img_url": "https://scdn.veryfi.com/receipts/c45f9514-0c48-4f49-9005-f5e5b39da401.jpg",
        "img_thumbnail_url": "https://scdn.veryfi.com/receipts/c45f9514-0c48-f5e5b39da401_t.jpg",
        "card_number": "4037",
        "category": "Meals & Entertainment",
        "currency_code": "USD",
        "date": "2018-06-23 19:56:00",
        "payment_type": "",
        "phone_number": "8183911059",
        "subtotal": 50.68,
        "tax": 10.00,
        "tip": 0.0,
        "total": 60.68,
        "vendor": {
            "address": "132 Palm Ave, Burbank, CA 91502, USA",
            "name": "Panera Bread",
            "vendor_logo": "https://cdn.veryfi.com/logos/us/910164080.png",
            "vendor_type": "cafe"
        },

        ...
    }
]

```