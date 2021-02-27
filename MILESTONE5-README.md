# Milestone 5

The code for milestone 5 is written in file `XML.java` starting from line 1247. It is pretty straightforward implementation and spawns a new thread to process the conversion.

To test this method, two test cases are written in file `XMLTest.java` as methods `testXmlToJsonAsyncSuccess` and `testXmlToJsonAsyncFail`. In order to get results from the spawned thread, a queue is made and result is passed through the queue. Two test cases both pass.

To run these test, run the command

```bash
./gradlew test
```


