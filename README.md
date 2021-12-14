# mongo-indexer

Create indexes from a specification file in a Mongo collections.

## Usage

    node index.js -d DATABASE -c COLLECTION -f FILE

## Options

    --host          -h      Mongo host (defaults to localhost).
    --port          -p      Mongo port (defaults to 27017).
    --database      -d      Name of Mongo database.
    --collection    -c      Name of Mongo collection.
    --file          -f      File containing index specifications.

## Details

To use a specification file, it must be in JSON format and stored inside the *definitions/* folder. Some example files are provided.

Each file contains an array of JSON objects, each object specifying one index to apply to the Mongo collection. Each object must contain at least two properties: name (the internal name used by Mongo for the index) and index (the field to create the index on). Any additional properties supported by Mongo can be specified in each object, so complex and multi-field indexes can be created.
