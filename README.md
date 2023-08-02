# Data Engineer Interview

In this interview exercise, you will architect – and implement part of – a hypothetical voter data ETL pipeline.

The pipeline will need to read dirty data from various structured sources (E.g. CSV county voter files, GeoJSON shape files, voter scores from BigQuery, etc) and produce a clean voter database cut for specific down-ballot races.

## Part 1: Data Modeling (20m)

Our system will use a simplified model of "Voter Data". It will be required to manage the following kinds of models:

 - Person
 - Phone
 - Address
 - Score

Use the SQL files in `/models` to define the tables, schemas and, relationships for these four models in the SQL flavor of your preference. Feel free to create additional files if required.

## Part 2: ETL Architecture (30m)

We will use [https://excalidraw.com](https://excalidraw.com) to diagram a potential ETL / ELT / ELTL architecture to ingest files that contain data from the models we defined in Part 1.

Assume that inbound data may contain partial models, dirty inputs, and arrive in a variety of formats. You may use any libraries, or platforms you have experience with.

## Part 3: File Parsing (40m)

Congrats: the team has decided to move forward with your data processing architecutre!

However, we've made the choice to standardize our input files' format to Parquet in a pre-processing step to help standardize the many different types of files that user may request we load into their accounts.

Inside the `/src` folder, let's begin to implement this pre-processing step in Python. Your implemention should be able to:

 - Accept multiple types of input files. Feel free to use the `/data` folder for examples, though this is not exhaustive.
 - Emit a valid Parquet file with the same schema and data contents as the input.
 - Be maintainable, extensible, and scale effectively for large files.

Feel free to use any libraries available on [pypi.org](pypi.org) to accomplish this task.
