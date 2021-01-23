# Milestone 2

## Brief

The two new methods are in `XML.java`.

The according newly added unit tests are in `XMLTest.java`.

The forked repo can be found at https://github.com/gwy15/JSON-java/tree/feat/milestone2. Please notice that it's on branch `milestone2` instead of `main` or `master`.

## Task 1

For the task1 in milestone2, considering that the search actually can be done before the parse is finished, I added a new `parse` method that deviated from the original one in that it accepts a search query and a "stack of paths", so that once these two matches on tag close event, the parse don't need to go any further and can directly return.

## Task 2

Task 2, however, still requires the whole body to be parsed in order to get the XML format then pick the tree from it to replace. Therefore as far I as know there are no obvious shortcut to it.

