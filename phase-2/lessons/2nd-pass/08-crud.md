# CRUD

In computer programming, create, read, update and delete (as an acronym CRUD or possibly a Backronym) (Sometimes called SCRUD with an "S" for Search) are the four basic functions of persistent storage.

- Create
- Read
- Update
- Delete

# Applied to Web Services


-RESTful API HTTP methods

| Resource | GET | PUT | POST | DELETE |
|-------------------------------------------------------:|:----------------------------------------------------------------------------:|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------|
| Collection URI, such as `http://example.com/resources` | **List** the URIs and perhaps other details of the collection's members.  |  **Replace** the entire collection with another collection. | **Create** a new entry in the collection. The new entry's URI is assigned automatically and is usually returned by the operation. |   **Delete** the entire collection. |
|Element URI, such as `http://example.com/resources/item17` | **Retrieve** a representation of the addressed member of the collection, expressed in an appropriate Internet media type. |  **Replace** the addressed member of the collection, or if it doesn't exist, create it. | Not generally used. Treat the addressed member as a collection in its own right and create a new entry in it. |  **Delete** the addressed member of the collection. |

# Resources

- [CRUD in Wikipedia](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete)
- [CRUD and RESTful](http://en.wikipedia.org/wiki/Representational_state_transfer#Applied_to_web_services)