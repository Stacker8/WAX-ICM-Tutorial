# WAX-ICM-Tutorial

**In the following tutorial I will give some examples for all requests, that are used for the ICM-API. For these examples I use NodeJS and the NPM-Package [Axios](https://www.npmjs.com/package/axios)**

## Before you start
To use the ICM-API you need to get your *"Creator-APIKey"*. If you send any requests without that APIKey, you will get the following output:
```javascript
{ 
  success: false, 
  message: 'Authentication required' 
}
```

### How to get your APIKey

First of all visit the official WAX-Creator site. [Click here](https://creator.wax.io)

Once the page is loaded, click at the top right on your username. A dropdown menu will pop up. At that menu click on the second list entry called **Account**.

![](https://i.imgur.com/MeeWsYw.png)

Now you find the button that says "ENABLE API KEY". If you found it, click on it.

![](https://i.imgur.com/RTy1phE.png)

The WAX-Creator will generate an APIKey and display it on the same site. Now you can copy and paste it in your application.

![](https://i.imgur.com/spBn5S8.png)
