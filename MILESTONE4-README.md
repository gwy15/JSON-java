# Milestone 4

For the milestone 4, I implemented the `toStream` method of `JSONObject` in file `JSONObject.java`.

The `toStream` method generates a JSONObject-stream from JSONObject. This stream iterates through
`JSONObject`'s first layer of children and return only those that has value typed as
`JSONObject`.

For example, `{"a": {}, "b": 1, "c": {"d": {}}}.toStream()` will iterate through
`(a, {})`, `(c, {"d": {}})` and skip `(b, 1)`.

Internally, this method first generates an iterator then use `StreamSupport.stream` and `Spliterators.spliteratorUnknownSize` to convert the iterator to `Stream`. The iterator is pretty straight forward: it stores the `JSONObject` inside along with an iterator of its keys. When iterating, it forwards the key iterator until a key with type `JSONObject` is found.

Two test cases are in written in file `JSONObjectTest.java` with the name `testToStream` and `testToStreamMut`. The first one use `Stream`'s methods to test that the stream is implemented correctly. The second one try to manipulate the streamed object and expect the changes are also applied to the original `JSONObject`. Both the test cases passed.

To run the test cases, run

```bash
./gradlew test
```
