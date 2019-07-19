# Search
### Here you can search for submissions that use the market_name parameter

```javascript
const axios = require('axios');

axios('https://api-icm.wax.io/api/IItemSubmission/search', {
        method: 'get',
        data: {
            "api_token": YOUR_API_KEY,
            "q": Q,
        },
    })
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error.response.data);
    });
```

**For this request there is one required and one non-required parameter**

Required
```javascript
{
  "api_token": YOUR_API_KEY[string],
}
```

Non-Required
```javascript
{
  "q": Q[string]
}
```

**If the request was successfully posted we get following output**
```javascript
{ 
  success: true, 
  message: null, 
  submissions: [ARRAY of submission objects]
}
```
[Submission Object](https://github.com/worldwide-asset-exchange/wax-item-creation-management/blob/master/IItemSubmission.md#standard-item-submission-object)
