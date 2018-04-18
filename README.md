# knex-gists
Gists of Knex:

This sets up the development environment and connecting it to the library and exporting it:

const environment = process.env.NODE_ENV || 'development';
const config = require('./knexfile');
const environmentConfig = config[environment];
const knex = require('knex');
const connection = knex(environmentConfig);

module.exports = connection;
