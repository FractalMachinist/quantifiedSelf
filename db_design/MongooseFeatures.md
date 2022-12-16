# Schema
https://mongoosejs.com/docs/guide.html
Schemas define what the data in a collection will look like.
## Methods
Schemas can define methods, statics, and query helper functions which will be available on any model using that schema.
## Indexes
Schemas can define indexes and indexing behaviors.
## Virtuals
Virtuals are attributes that masquerade as part of a document, but in fact are computed views. Virtuals can also provide setters.
## Options
- collection
    - Specify the name of the collection the schema should populate
- discriminatorKey
    - Relates to Mongoose's type overlapping and inheritance
- timeseries
    - https://www.mongodb.com/docs/manual/core/timeseries-collections/
    - MongoDB supports timeseries data
    - Comprised of generally 3 components:
        - Time
        - Metadata
        - Measurements
- timestamps
    - Manage 'createdAt' and 'updatedAt' fields
- pluginTags
    - Allows associating a schema conditionally for global plugins


## Plugins
https://mongoosejs.com/docs/plugins.html
Plugins are a tool for reusing logic in multiple schemas.

## ES6 Classes
https://mongoosejs.com/docs/guide.html#es6-classes

## Descriminators
https://mongoosejs.com/docs/discriminators.html
Discriminators are a schema inheritance mechanism. They enable you to have multiple models with overlapping schemas on top of the same underlying MongoDB collection.

A common model is defined across the collection, and other models are constructed to inherit from that model and exist in the same collection, but with separate models based on extending schemas of their own.

# Model
Models provide functionality for querying and interacting with data in a collection.