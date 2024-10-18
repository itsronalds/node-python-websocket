# node-python-websocket

## General Information

Test project where we create a server with native Node.js and use a Python client to send live invoices using WebSockets.

## Requirements

- You must have Node.js installed
- You must have Python installed
- You need SQL Server or a cloud instance of this database

## Clone the Project

```bash
git clone https://github.com/itsronalds/node-python-websocket
```

## Setting Up the Node.js Server

### Install Dependencies

In the project root, first navigate to the `server` folder using:

```bash
cd server
```

Then, run the following command:

```bash
npm i
```

> This will install all the server dependencies

### Configure Environment Variables

Our project has two environment variables:

- PORT: the port where our server will run
- MSSQL_CONNECTION_STRING: the connection string to the database hosted on Azure. `You can use a local database, the model is in db/model.sql`

```bash
# File: .env

PORT=8000
MSSQL_CONNECTION_STRING=Server=server_name,port;Database=database_name;User Id=user;Password=password;Encrypt=true
```

> Replace `server_name`, `port`, `database_name`, `user`, and `password` with the correct values for your database

### Run the Server

After completing the previous steps, the only thing left is to start the server:

```bash
npm start
```

## Set Up the Python Client

### Create a Virtual Environment

In the project root, first navigate to the `client` folder using:

```bash
cd client
```

Then, run the following command to create the virtual environment:

```bash
python -m venv venv
```

> You'll see a folder named `venv`, which will store our dependencies

### Activate the Virtual Environment

In the `client` folder, run the following command:

```bash
# On Windows
venv\scripts\activate
```

### Install Dependencies

Now, with `venv` active, it's time to install our dependencies:

```bash
pip install -r requirements.txt
```

> This will install all the client dependencies

### Run the Client

After completing the previous steps, the only thing left is to start the client:

```bash
py main.py
```

## Everything should work fine 🚀
