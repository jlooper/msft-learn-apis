# Authentication Strategies

While the Metropolitan Museum's API is open to the public without the need to authenticate, and requests only that users "limit request rate to 80 requests per second", this level of openness for APIs is a little unusual. Usually, the organization managing a publicly-facing API will require some kind of authentication in order to access it to protect itself from unwanted over usage of the endpoints.

If your API requires authentication, you won't be able to make calls to get data directly via URL calls. Instead, you will need to leverage `request headers`, an object that is sent with your request using an HTTP call.

> Note, always use authentication over a secure `https` connection

## Using HTTP protocols to authenticate

The HTTP protocol makes available to the developer several authentication strategies, including 'Basic' and 'Bearer'. Basic authentication is inherently insecure as it requires passing a username and password through a request header directly, which might look like this:

`Authorization: Basic abcdef12345==`

 You are more likely to see Bearer authentication, which requires a token, retrieved prior to the authentication call, that must be passed in the request header:

 `Authorization: Bearer <mytoken>`

## Using API keys to authenticate

API keys are very common in API architecture, and they can show up in various places: passed via body data as JSON, sent through a query string, or sent via a custom header or an authorization header.

While keys are an easy way to form a handshake between your code and an API, they are not inherently secure, as anyone in theory could use a key if they can intercept it via a network call. 

> It's a good idea to store your API keys in the cloud and access them using a function that calls an environment variable, but that's out of scope for this tutorial!

While this topic can easily get very complicated, the most common way to authenticate to use an API is by using an API key. In the next section, you will  