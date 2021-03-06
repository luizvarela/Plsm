# Plasm - Ecto model generation

Plasm generates Ecto models based on existing database tables in your database. Currently, Ecto only allows the ability to create migrations that creates new tables/schemas. If you have an existing project that you want to add Ecto support for you would have to hand code the models. This can be tedious for tables that have many columns. 


## Dependencies
The only thing required are Erlang, Mix and the ODBC driver for the database that you are working with. Currently we only support MySql but other database support is coming soon. All data access is done through Erlang so we limit dependencies on 3rd party libraries

## Running Plasm

First, in order to run plasm you need to generate a config file. You do this by running

`mix plasm.config`

This will create a skeleton config file. You will need to make your changes in order to run Plasm succesfully.

Once you have your config file generated then you are ready to run plasm. You do this by running 

`mix plasm`

The model files are generated in the folder that you are running from.

## Getting Plasm

You can add 

`{:plasm_ecto, ">= 0.2.0"}`

to deps in your mix.exs and that will download the package for you

## Forthcoming updates

The plan is to add the following features:
  * Support for other databases
  * the ability to save to other paths
  * better error handling
  * more unit tests

If you have any questions you can reach me via email at jon@dontbreakthebuild.com
