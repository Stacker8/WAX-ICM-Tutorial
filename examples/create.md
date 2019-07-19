# Create
### Here you can create a new item

```javascript
const axios = require('axios');

axios('https://api-icm.wax.io/api/IItemSubmission/create', {
        method: 'post',
        data: {
            "api_token": YOUR_API_KEY,
            "internal_app_id": 14,
            "name": "Test Item",
            "market_name": "TEST ITEM",
            "image_generic": "https://static.wax.io/d-img/dynamic-apps/img/phpfdn9tp-1db5e2fb79.png",
            "amount": 100,
            "color": "white",
            "rarity_name": "Legendary",
            "collection_name": "Test Collection",
            "external_id": 1,
            "instant_sell_enabled": true,
            "instant_sell_value": 0.03,
            "json_attributes": {
                "Verified_Authentic": "Yes",
                "product_box_display": "collection, class, mana, hp"
            }
        },
    })
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error.response.data);
    });
```

**For this request there is seven required and seven non-requird parameter**

Required
```javascript
{
  "api_token": YOUR_API_KEY[string],
  "internal_app_id": INTERNAL_APP_ID[int],
  "name": NAME[string],
  "market_name": MARKET_NAME[string],
  "image_generic": IMAGE_GENERIC[string],
  "amount": AMOUNT[Int],
  "color": COLOR[strimg],
}
```

Non-Required
```javascript
{
  "rarity_name": RARITY_NAME[string],
  "collection_name": COLLECTION_NAME[string],
  "external_id": EXTERNAL_ID[int],
  "instant_sell_enabled": INSTANT_SELL_ENABLED[boolean],
  "instant_sell_value": INSTANT_SELL_VALUE[int],
  "json_attributes": {
    "Verified_Authentic": VERIFIED_AUTHENTIC[string],
    "product_box_display": PRODUCT_BOX_DISPLAY[string]
  }
}
```

For more information [click here](https://github.com/worldwide-asset-exchange/wax-item-creation-management/blob/master/IItemSubmission/create.md)

**If the request was successfully posted we get following output**
```javascript
{ 
  success: true,
  message: null,
  submission_id: 10
}
```

