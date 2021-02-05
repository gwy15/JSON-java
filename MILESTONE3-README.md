# Milestone 3

The `keyTransformer` is typed as `Function<String, String>` that takes a string and returns a string.

By putting the transforming process in the library, we can avoid iterate through the json object again after creating it and instead
do it in the creating process.

To be more specific, the `context.accumulate`, which is when the tags are appended to the response object, are accepting keys after
the process of `keyTransformer`. By doing this we can reduce the extra iteration and thus saves overhead.

Generally speaking, the more complex the json object is with respect to the tree structure, the more overhead we can save.

Unittests are written in `testXmlToJsonWithKeyTransform` method in `XMLTest.java` file.


## Run
To run the unit tests, run command `./gradlew test`. Please know that java 8 is required.
