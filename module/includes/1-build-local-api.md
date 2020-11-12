# Exercise - Building a local API

Before any API is deployed to the cloud, it probably is developed locally by a developer like you. You can create an API right on your local computer (of course, nobody externally will be able to use it, but that's not its purpose).

Run the following command on your command line or terminal:

`npm install -g json-server`.

This package, [JSON-Server](https://github.com/typicode/json-server), creates a "full fake REST API server" and is useful for prototyping and learning.

Then, using a text editor or Visual Studio Code, create a file on your local computer called `db.json`:

```
{
  "objects": [
    { "id": 1, "item": "Lise with a Parasol", "artist": "Pierre Auguste Renoir", "collection":"Museum Folkwang, Essen, Germany", "date":"1867"},
    { "id": 2, "item": "The Theatre Box", "artist": "Pierre Auguste Renoir", "collection":"Courtauld Gallery, London, England", "date":"1874"},
    { "id": 3, "item": "Dance in the City", "artist": "Pierre Auguste Renoir", "collection":"Musée d'Orsay, Paris, France", "date":"1883"},
    { "id": 4, "item": "Dance in the Country", "artist": "Pierre Auguste Renoir", "collection":"Musée d'Orsay, Paris, France", "date":"1883"}
  ]
}
```
This JSON file is a mocked version of a database. You can use `json-server` to query this data.

In your terminal, navigate to the location where you added `db.json` and type `json-server --watch db.json`. The server will run on port 3000 and you can query it via a specially-formatted URL. Try typing in a browser URL bar: `http://localhost:3000/objects`. You'll see all the objects in your database listed in neat JSON format.

Try using the URL to query this dataset: `http://localhost:3000/objects/1` will display the item with id `1`. 

You may have noticed that your API call consists of a few parts. The four major parts of a REST API call include the endpoint, the method, the headers, and the data (or body).

You can also search by an item name: `http://localhost:3000/objects?item=Lise%20with%20a%20Parasol`. 

These type of queries demonstrate two facts: you need to format queries passing through a URL with special characters to handle the spaces in the title, and you are using a `query string` to query the objects data by using the format `objects?item=`. This format is a standard REST API strategy of formatting queries. 

Take a look at your browser's developer tools in the network tab to observe the way the API you built is behaving. If you refresh your browser, you can discover that behind the scenes you are using `GET` to retrieve data to be shown in the browser.

In our call, you called an endpoint via a URL: `http://localhost:3000/objects`. The method used is `GET`. You don't need any headers in your call at present (you'll learn more about headers shortly). The data that is returned is the same that is stored in your `db.json` file, filtered by the query.
