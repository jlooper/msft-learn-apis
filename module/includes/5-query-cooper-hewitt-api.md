# Exercise - Query the Cooper Hewitt API

Now that you have discovered some interesting collections at the Metropolitan Museum, let's look at a different museum API, that of the Cooper Hewitt. This museum is part of the Smithsonian, and is the US's National Design Museum. Its collection is comprised of interesting and notable design, from Dyson fans to antique shoes.

To access this API, you need an access token and an API key that acts as its authenticator. Go to the [API homepage](https://collection.cooperhewitt.org/api/) and sign up for a key. To do this, create an account. Once your account is created, you can create an access token for yourself.

> Why create an access token? This API uses [OAuth (version 2)](https://collection.cooperhewitt.org/api/oauth2/), which requires tokens to monitor and limit access to the API. Once you have a token created, you can create an API key. This API key works with the access token to ensure that you have the authority to access the API in the way that you have set up the token.

Once you have created a token and authenticated it with an API key, you can start sending that token in the URL of a test API call. Let's see what we can find in the Cooper Hewitt Design Museum!

Let's say you are interested in Art Nouveau, and you'd like to see what objects exist in the collection from this era. The API will allow you to get an ID for the era in question, and query it to get a url with a collection specified for the era.

> For the following queries, obtain an access token as noted above and paste it in to the query where specified.

To find the Art Nouveau objects, query the API thus: `https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.periods.getList&access_token=<your-token>&page=1&per_page=100`. This query specifies that you need to append the page you will retrieve and the number of elements returned per page.

By querying the API, a URL is returned in the response with a list of Art Nouveau objects available for perusal (including some famous Mucha posters): `https://collection.cooperhewitt.org/periods/35417231/`. Take a look. What other eras can you discover by querying this API?