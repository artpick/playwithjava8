# Play with java8

## Create a list of a specified element property.
```java
/**
 * For all the elements of the input list, create a list of a specific property.
 
 * @param allElements : go over it.
 * @param specificProperty : the property / getter we will make the list from.
 * @param <U>
 * @param <T>
 * @return
 */
private static <U, T> List<T> remapList(final List<U> allElements, final Function<U,T> specificProperty) {
       return Optional.ofNullable(allElements)
                    .map( al -> al.stream().map(a -> specificProperty.apply(a)).collect(Collectors.toList()))
                    .orElse(null);
}
```
