# Refill
### Here you can request a refill for your own created items

```javascript
const axios = require('axios');

axios('https://api-icm.wax.io/api/IItemSubmission/refill', {
        method: 'post',
        data: {
            "api_token": YOUR_API_KEY,
            "submission_id": SUBMISSION_ID,
            "number_of_items_to_refill": NUMBER_OF_ITEMS_TO_REFILL
        },
    })
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error.response.data);
    });
```

**For this request there are three required parameter**

Required
```javascript
{
  "api_token": YOUR_API_KEY[string],
  "submission_id": SUBMISSION_ID[int],
  "number_of_items_to_refill": NUMBER_OF_ITEMS_TO_REFILL[int]
}
```

**If the request was successfully posted we get following output**
```javascript
{ 
  success: true, 
  message: 'Your request was received.' 
}
```
