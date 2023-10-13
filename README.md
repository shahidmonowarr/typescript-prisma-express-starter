# TypeScript - Prisma - Express Starter Pack

This guide will walk you through the process of setting up the TypeScript-Prisma Starter project. By following these steps, you will clone the project, install dependencies, and configure Prisma for database management. Let's get started!

## Installation Steps

### Follow these steps to clone and set up starter project:

1. `Clone the project:` Open your terminal or command prompt and run the following command to clone the project repository:

```bash
git clone https://github.com/shahidmonowarr/typescript-prisma-express-starter.git typescript-prisma-express-starter
```

2. `Navigate into the project directory:` Use the cd command to navigate into the project directory:

```bash
cd typescript-prisma-express-starter
```

3. `Install project dependencies:` Next, install the project dependencies by running the following command:

```bash
yarn install
```

4. Configure Prisma and the database connection:

- Open the prisma/schema.prisma file and configure your database connection details.

```bash
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}
```

- Create a .env file in the project root directory and set the DATABASE_URL environment variable. Replace the placeholders with your database connection details:

```bash
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE?schema=SCHEMA"
```

5. Creating the database schema

- Create the database schema: Use the following command to create the database schema. Just go to the prisma/schema.prisma file and uncomment the model User and run the following command:

```bash
// test model for prisma
// uncomment to test prisma

// model User {
//   id    Int     @id @default(autoincrement())
//   email String  @unique
//   name  String?
// }
```

6. Migrate the database schema: Use the following command to create and apply the initial database schema:

```bash
npx prisma migrate dev --name init
```

This command creates a new migration file based on your schema changes and applies it to your database.

6. `Install Prisma Client:` Install the Prisma Client library by running the following command:

```bash
yarn add @prisma/client
```

This command installs the Prisma Client, which provides an interface to interact with your database.

That's it! You have successfully set up the Starter project. You can now start exploring and working with the codebase. Refer to the project documentation or README for further instructions on how to run the project.

Happy coding!
