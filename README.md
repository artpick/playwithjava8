# Play with java8

## Create a list of a specified element property.
```
/**
 * For all the elements of the input list, create a list of a specific property.
 
 * @param allElements : go over it.
 * @param specificProperty : the property / getter we will make the list from.
 * @param <U>
 * @param <T>
 * @return
 */
private static <U, T> List<T> remapList(final List<U> allElements, final Function<U,T> specificProperty) {
  if (CollectionUtils.isEmpty(allElements)) {
    return null;
  }
  return allElements.stream().map(a -> specificProperty.apply(a)).collect(Collectors.toList());
}
```
