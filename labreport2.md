# Lab Report 2

## Part 1: String Server

**Code for String Server**
![Image](https://user-images.githubusercontent.com/86041345/215351849-6830247c-52d8-42f6-b860-58a41362cba2.png)

**Adding a Message**
![Image](https://user-images.githubusercontent.com/86041345/215352081-520a58d6-e6a1-40a0-8b81-1ee431e530c3.png)
The URL above calls the `handleRequest` method, which takes said URL as an argument. This method calls `getPath` to
find the URL's path and calls `contains` to check if the path contains `"add-message"` (the argument of `contains`).
Since the given path meets this condition, `getQuery` is used to find the URL's query, and `split` is used to separate
the query into two strings, based on the left and right sides of the `"="` (the argument of `split`). These strings,
`"s"` and `"Why can't skeletons play church music?"`, are saved in an array, `parameters`.

Next, `equals` is used to check if `parameters[0]` is equal to `"s"` (the argument of `equals`). Since this is true, 
`"\n" + parameters[1]` is added to an ArrayList called `strings`, which tracks the messages added. This element in
`strings` is copied to a string variable called `allStrings`, which is displayed on the website.

**Adding Another Message**
![Image](https://user-images.githubusercontent.com/86041345/215352161-ff36ff4a-b447-45f7-a58c-627039bad038.png)
Just as in the previous example, the URL above calls the `handleRequest` method, which takes said URL as an argument.
This method calls `getPath` to find the URL's path and calls `contains` to check if the path contains `"add-message"` 
(the argument of `contains`). Since the given path meets this condition, `getQuery` is used to find the URL's query, 
and `split` is used to separate the query into two strings, based on the left and right sides of the `"="` (the argument
of `split`). These strings, `"s"` and `"They don't have any organs!"`, are saved in the `parameters` array.

Next, `equals` is used to check if `parameters[0]` is equal to `"s"` (the argument of `equals`). Since this is true, 
`"\n" + parameters[1]` is added to the `strings` ArrayList. There are now two elements in `strings` (one from the 
previous example, one from this example), so both of these strings are concatenated to the `allStrings` variable, which
is displayed on the website.

---

## Part 2: Debugging Array Methods

I am testing the method `reverseInPlace`, which is supposed to return the elements of the input array in reversed order.

**Failure-Inducing Input**
```
@Test
public void testReverseInPlace1() {
  int[] input1 = {7, 92, 18, 34, 65, 100};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 100, 65, 34, 18, 92, 7 }, input1);
}
```

**Asymptomatic Input**
```
@Test 
public void testReverseInPlace2() {
  int[] input2 = { 37, 24, 15, 24, 37 };
  ArrayExamples.reverseInPlace(input2);
  assertArrayEquals(new int[]{ 37, 24, 15, 24, 37 }, input2);
}
```

**The Symptom**
![Image](https://user-images.githubusercontent.com/86041345/215370130-cb354853-e28c-4abc-b618-7e67f48cc15a.png)

**The Bug: Before**
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

**The Bug: After**
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length / 2; i += 1) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```
This change addresses the issue by switching elements in the array instead of replacing / writing over them.
For example, the new code switches the first and last elements in the array by storing the first element in a
variable, ```temp```, setting the first element equal to the last, and setting the last element equal to ```temp```.
Unlike the previous code, which would replace the first element completely, the new code reverses the elements
in the array correctly.

## Part 3: New Concepts
Something new that I've learned from lab is that you can use JUnit tests in order to identify bugs. I found that
it is important to create multiple tests that each use different inputs because some may be failure-inducing inputs 
that show symptoms of bugs in your code.
