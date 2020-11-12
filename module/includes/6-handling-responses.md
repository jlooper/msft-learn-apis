# Handling Responses

In many situations, it's important to know the status codes that are sent back by a RESTful API. What if there's a server error? What if there's no data to be sent back? What if there's an authentication error? In any of these cases, it's useful to watch for codes, so that you can tell the front-end user that there's a problem.

Try, for example, a query like this in your browser: `https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.periods.getList&access_token=xxxxx&page=1&per_page=100`.

The API will return a code of `400`: this is an error of access as your access token is invalid.

It is useful to learn about the [various access errors](https://api.collection.cooperhewitt.org/rest/?method=cooperhewitt.periods.getList&access_token=xxxxx&page=1&per_page=100) you might encounter. Normally a `200` code means 'all is well' and you can continue to display the query results. It's just as useful to be able to triage errors and display appropriate message handling them.

> A memorable way of looking at errors is `http.cat` by Tomomi Imuri. You'll never forget that `200` means 'ok'!
