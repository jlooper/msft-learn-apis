# Title

*Explore The Art World with RESTful APIs*

## Role(s)

- *student*

## Level

- *beginner*

## Product(s)

- *Visual Studio Code*

## Prerequisites

- *Development Environment with VS Code Installed*
- *Internet connectivity*

## Summary

*In this module, you will learn about APIs, the "Application Programming Interfaces" that act like the 'handshake' between a web site's frontend and backend, with specific focus on RESTful APIs. You will first create a simple local API with a .json file and then work with APIs from the the Victoria and Albert Museum and the Cooper Hewitt Museum to learn about the ways to securely interact with third-party interfaces.*

## Learning objectives

1. REpresentational State Transfer - a REST primer
2. Learn about the ways to connect to a RESTful API
3. Build a basic API locally
4. Authentication strategies
5. Query your first API to search for objects at Metropolitan Museum
6. Work with tokens and query parameters to find an unusual design object at the Cooper Hewitt Museum
7. Handle responses, including errors by understanding HTTP codes
8. Using libraries to help with your queries (axios)
9. Other types of APIs you might encounter (The Met's CSV strategy)

## Chunk your content into subtasks

Identify the subtasks of *Explore The Art World with RESTful APIs*




| Subtask                               | Covers learning objective # | How will you assess it: **Exercise or Knowledge check**? |
| ------------------------------------- | --------------------------- | -------------------------------------------------------- |
| Introduction: What is an API          | 1                           | --                                                       |
| Scaffold a local API structure        | 2                           | exercise                                                 |
| Connecting to a 3rd party API         | 3                           | knowledge check                                          |
| Query the Met API using a Query Parameter | 4                           | exercise                                                 |
| Authentication strategies             | 5                           | --                                                       |
| Query the Cooper Hewitt               | 6                           | exercise                                                 |
| Handling responses                    | 7                           | --                                                       |
| Using libraries                       | 8                           | knowledge check                                          |
| More APIs                             | 9                           | --                                                       |
| Knowledge check                       | --                          | --                                                       |

## Outline the units

*Add more units as needed for your content*

1. **Introduction**

You're a web developer who needs to learn how to use third-party content within your app. Specifically, you need to create a search for an art museum's database to discover new art. Do you have to create it yourself from scratch, or can you use an API to make that handshake between your frontend and backend?

1. **Learning-content unit title**

    List the content that will enable the learner to *subtask*:

    - What is an API
        Define the concept, providing examples of how they can be used
    - Scaffold a local API structure
        Using a basic .json file and JSON-server, create a mockup of an API to learn how data is structured to be retrieved (https://codingthesmartway.com/create-a-rest-api-with-json-server/)
    - Connecting to a 3rd party API
        You're ready to try your hand at discovering art! Query the Victoria and Albert's open API to find a painting of a dog https://www.vam.ac.uk/api/json/museumobject/search?q=paintings+of+dogs
    - Deepening your understanding of the 'handshake' between the frontend and backend by using Authentication
        Some APIs require special authentication. Learn about getting keys and using them in headers, searching for designs with cats in the Cooper Hewitt's API
    - Sometimes the response isn't what you expect. Learn about status codes and how to handle them (https://http.cat/ via Tomomi)
    - There are some helpers to query APIs, so let's learn about them for the various languages:
       Axios for JavaScript
       Requests for Python
    - Not all APIs are built with a nice JSON return. Discover other types of API structures like XML, SOAP, and even flat .csv files. Experiment with querying the Metropolitan Museum's .csv 'API'.
    
   
 Notes: we have written permission from the Cooper Hewitt to use their API, the Metropolitan is open to commercial use, and we are checking with the V&A.
