# Read
### Here you can fetch the submission data from an item

```javascript
const axios = require('axios');

axios('https://api-icm.wax.io/api/IItemSubmission/read', {
        method: 'get',
        data: {
            "api_token": YOUR_API_KEY,
            "submission_id": SUBMISSION_ID,
        },
    })
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error.response.data);
    });
```

**For this request there is one required and one non-requird parameter**

Required
```javascript
{
  "api_token": YOUR_API_KEY[string],
}
```

Non-Required
```javascript
{
  "submission_id": SUBMISSION_ID[int],
}
```

*Note*

If no SUBMISSION_ID is provided, will return all submissions made by you.


**If the request was successfully posted we get following output**
```javascript
{ 
  success: true,
  message: null,
  submissions: [ARRAY of submission objects] 
}
```
[Submission Object](https://github.com/worldwide-asset-exchange/wax-item-creation-management/blob/master/IItemSubmission.md#standard-item-submission-object)

