# AYGO-02

# Endpoints for the Microservices

## Users MS

* `GET /users` - Get all users
* `GET /users?offset=<num>&limit=<num>` - Get users with pagination
* `GET /users/{id}` - Get user by id
* `POST /users` - Create user
* `PUT /users/{id}` - Update user
* `DELETE /users/{id}` - Delete user

## Tweets MS

* `GET /tweets` - Get all tweets
* `GET /tweets?offset=<num>&limit=<num>` - Get tweets with pagination
* `GET /tweets/{id}` - Get tweet by id
* `POST /tweets` - Create tweet
* `PUT /tweets/{id}` - Update tweet
* `DELETE /tweets/{id}` - Delete tweet
* `GET /tweets/user/{id}` - Get all tweets by user id
* `GET /tweets/hashtag/{hashtag}` - Get all tweets by hashtag
* `GET /tweets/hashtag/{hashtag}/user/{id}` - Get all tweets by hashtag and user id

## Follow MS

* `GET /follows` - Get all follows
* `GET /follows/offest/{offset}/limit/{limit}` - Get follows with pagination
* `GET /follows/{id}` - Get follow by id
* `POST /follows` - Create follow
* `DELETE /follows/{id}` - Delete follow
* `GET /follows/user/{id}` - Get all follows by user id
* `GET /follows/following/{id}` - Get all follows by following id
* `GET /follows/user/{id}/following/{id}` - Get follow by user id and following id
* `GET /follows/user/{id}/following` - Get all following by user id
* `GET /follows/user/{id}/followers` - Get all followers by user id

## Home MS

* `POST /home/user/{id}` - Send configuration to the home of the user

## Search MS

* `GET /search/user/{id}` - Get all users by user id
* `GET /search/tweet/{id}` - Get all tweets by user id
* `GET /search/hashtag/{hashtag}` - Get all tweets by hashtag
* `GET /search/trending` - Get all trending hashtags

## Comments MS

* `GET /comments` - Get all comments
* `GET /comments?offset=<num>&limit=<num>` - Get comments with pagination
* `GET /comments/{id}` - Get comment by id
* `POST /comments` - Create comment
* `PUT /comments/{id}` - Update comment
* `DELETE /comments/{id}` - Delete comment
* `GET /comments/tweet/{id}` - Get all comments by tweet id
* `GET /comments/tweet/{id}?offset=<num>&limit=<num>` - Get all comments by tweet id with offset and limit

## Representation

JSON is used for all requests and responses.

## User

```json
{
  "id": "string",
  "userName": "string",
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "tweets": [
    "string"
  ],
  "follow": "Follow",
  "createdAt": "string",
  "updatedAt": "string"
}
```

## Tweet

```json
{
  "id": "string",
  "date": "string",
  "msg": "string",
  "userId": "string",
  "media": [
    "byte"
  ],
  "likes": "integer",
  "retweets": "integer",
  "createdAt": "string",
  "updatedAt": "string"
}
```

## Follow

```json
{
  "id": "string",
  "userId": "string",
  "followersId": [
    "string"
  ],
  "followeesId": [
    "string"
  ],
  "createdAt": "string",
  "updatedAt": "string"
}
```

## Comment

```json
{
  "id": "string",
  "tweetId": "string",
  "date": "string",
  "msg": "string",
  "userId": "string",
  "media": [
    "byte"
  ],
  "likes": "integer",
  "retweets": "integer",
  "createdAt": "string",
  "updatedAt": "string"
}
```

## Error

```json
{
  "error": "string",
  "message": "string",
  "statusCode": "number"
}
```

# Authors

- [Julian Alvarez Villamil](https://github.com/julian36alvarez)
- [Julian Benitez Gutierrez](https://github.com/julianbenitez99)