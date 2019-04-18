# PizzaQL Docs :pizza:

## About

The goal of this project is to provide a modern and easy to use order management system with order placement form as well. You can track progress in our TODO list :smile: 

More information coming soon. Please note that this project is currently **work in progress** and you shouldn't use it in production!

## Usage

Follow the following guides to start the app in development mode or build it in production mode :smile:

### Development

#### Prerequisites

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/)
- [Prisma CLI](https://www.prisma.io/docs/prisma-cli-and-configuration/using-the-prisma-cli-alx4/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Auth0 Account](https://auth0.com/)

#### Steps

1. Clone this repository:

```
git clone https://github.com/pizzaql/pizzaql && cd pizzaql
```

2. Configure backend

```
# Enter the `backend` directory
cd backend

# Deploy the database & Prisma ORM
docker-compose up -d && prisma deploy

# Start the GraphQL Yoga server
npm install && npm start
```

3. Configure frontend

```
# Go back and enter the `frontend` directory
cd .. && cd frontend

# Install required dependencies
npm install
```

4. Edit the `settings.js` file and include your Auth0's client id & domain:

```js
const clientID = process.env.CLIENTID || 'YOUR_AUTH0_CLIENTID';
const domain = process.env.DOMAIN || 'YOUR_AUTH0_DOMAIN';

export {
	clientID,
	domain
};
```

5. Start the application in the development mode:

```
npm run dev
```

6. Congrats! You now should have access to:

- GraphQL Playground at `http://localhost:4000/`
- Order placement form at `http://localhost:3000`
- Admin dashboard at `http://localhost:3000/admin` (you will need to login to see the list of orders)

### Production

To build the application in production mode, run:

```
npm run build
```

You can then run the optimized version of PizzaQL, by executing the following command:

```
npm start
```

## License

MIT
