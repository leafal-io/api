# /users/

## Request Body
Field | Description
------|------------
**query** | A user lookup query.

Lookup queries define what specified information of the user you want to use to look up their user info. The `username:leaf` query will look up a user by 
the username `leaf`. The `uuid:33286d41-c596-4b84-b0a9-6b556ac232da` query will look up a user with the UUID `33286d41-c596-4b84-b0a9-6b556ac232da`.

## Expected Response
Field | Description
------|------------
**id** | A numerical identifier unique to the user.
**username** | The user's login name.
**display_name** | The user's display name.

### Example
```javascript
{
    "uuid": "33286d41-c596-4b84-b0a9-6b556ac232da",
    "username": "leaf",
    "display_name": "leaf."
}
```

### Possible Errors
Error Code | What happened
-----------|--------------
**400: Bad Request** | Missing request body or missing user query. Error message is provided.
**404: Not Found** | A user matching the provided query could not be found.
**500: Server Error** | A database error occurred.
