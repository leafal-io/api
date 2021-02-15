# Users
## /users/

### GET Fields
Field | Description
------|------------
**query** | A user lookup query.

Lookup queries define what specified information of the user you want to use to look up their user info. The `username:leafal.io` query will look up a user by 
the username or profile URL `leafal.io`. The `id:1` query will look up a user with the User ID `1`.

### Expected response
Field | Description
------|------------
**id** | A numerical identifier unique to the user.
**name** | The displayed name of a user.
**banned** | Whether or not the user is banned from leafal.io.
**username** | The user's login name.
**role** | The user's role on the platform.
**url** | The user's Profile URL.
**avatar** | The relative path from `https://www.leafal.io` to the user's avatar.
**coin** | Contains information about the user's selected Avatar Coin.

```javascript
{
    "id": "1",
    "name": "leafal.io",
    "banned": false,
    "username": "leafal.io",
    "role": "staff",
    "url": "leafal.io",
    "avatar": "/assets/uploads/profile1-2.png",
    "coin": {
        "name": "transparent",
        "source": "transparent",
        "title": "Seamless",
        "desktop": "#00FFFFFF"
    }
}
```
