# Using Libraries

It's useful to test an API by sending queries over a browser's URL, complete with a query string populated by an access token, but in a production app, you might need to make a more complicated API call with various data assembled together to form a query.

Many developers, therefore, rely on libraries that standardize the process of working with APIs. For JavaScript developers, Axios is an excellent choice. Python programmers tend to use Request.

Imagine that you are passionate about clock radios, and are interested in the interesting collection of well-designed examples at the Cooper Hewitt. You would construct a query with your API access token with this format, given that you want paginated results and only results with images: 

`https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.search.collection&access_token=<your access token>&query=clock%20radio&has_images=true&page=1&per_page=100`, as specified in the museum's API documentation.

The first example that comes up is this slick example from the 1950s:

![1957 clock radio](https://images.collection.cooperhewitt.org/39369_1f0c462c864fbf4d_b.jpg)

> To test API endpoints, [Postman](https://www.postman.com/) is an excellent tool.

::: zone pivot="javascript"

var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.search.objects&query=clock&20;&page=1&per_page=100&access_token=yourtoken',
  headers: { }
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});

::: zone-end

::: zone pivot="python"

import requests

url = "https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.search.objects&query=fan&page=1&per_page=100&access_token=5a3c42c653014805fd1e06902631596f"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))


::: zone-end