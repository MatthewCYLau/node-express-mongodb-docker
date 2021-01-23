# Node Express MongoDB Docker

A reference project to containerise a Node Express app with Docker, with persistent database using MongoDB

## Run/Build Locally

In the project root directory, run this command:

```bash
docker build -t node-express-mongodb-docker . # builds Docker image
docker run -e JWT_SECRET='<your_super_secure_secret>' -e MONGO_URI='<your_mongodb_connection_url>' -p 80:5000 node-express-mongodb-docker # runs image in container; maps port 80 of your local machine, to port 5000 of container
```

- Make `POST` request to `http://localhost:8000/api/users` to create a user:

```json
{
  "email": "hello@world.com",
  "password": "password",
  "name": "John Doe"
}
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
