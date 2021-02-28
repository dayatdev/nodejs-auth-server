# nodejs-auth-server

Backend for nodejs auth

## Requirements

- Nodejs and NPM
- postgresql (local)

## Setup Database

  create .env file, or rename .env.example to .env

- user : postgres
- host : localhost
- password: postgres
- database: nodeauth
- port : 5432

1. Create Database 
    CREATE DATABASE nodeauth;
2. Create Table
    CREATE TABLE users (
      id SERIAL PRIMARY KEY NOT NULL,
      name VARCHAR(50) NULL,
      email VARCHAR(50) NOT NULL UNIQUE,
      image_identity VARCHAR NULL,
      username VARCHAR NULL UNIQUE,
      password VARCHAR NULL,
      registration_date timestamp(0) NULL
    );

## Install

  $ git clone https://github.com/dayatdev/nodejs-auth-server.git
  $ cd nodejs-auth-server
  $ npm install

## Run
  $ npm run dev
