# Upload-Image
### Here you can upload an image to use it later in the [create](./create.md) request

This request is a bit tricky, because we need to manage including an image in it. To do that we are going to use a NPM-Package called [Form-Data](https://www.npmjs.com/package/form-data) and the preinstalled [fs](https://nodejs.org/api/fs.html) module.

```javascript
const axios = require('axios'),
    fs = require('fs'),
    FormData = require('form-data'),
    form = new FormData();

form.append('image_name', 'Test');
form.append('image_file_to_upload', fs.createReadStream(__dirname + '/test.png'));
form.append('api_token', YOUR_API_KEY);

axios('https://api-icm.wax.io/api/IItemSubmission/upload-image', {
        method: 'post',
        data: form,
        headers: form.getHeaders()
    })
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error.response.data);
    });
```

**For this request there are two required and one non-required parameter**

Required
```javascript
form.append('api_token', YOUR_API_KEY[string]);
form.append('image_file_to_upload', fs.createReadStream(__dirname + PATH_TO_THE_IMAGE[string]));
```

Non-Required
```javascript
form.append('image_name', YOUR_CUSTOM_NAME[string]);
```

**If the file got successfully uploaded we get following output**
```javascript
{ 
  success: true,
  message: 'Your image was successfully uploaded.',
  image_url: 'https://static.wax.io/d-img/dynamic-apps/img/phpfdn9tp-1db5e2fb79.png' 
}
```
