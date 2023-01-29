# Lab Report 2

## Part 1: String Server

**Code for String Server**
![Image](https://user-images.githubusercontent.com/86041345/215351849-6830247c-52d8-42f6-b860-58a41362cba2.png)

**Adding a Message**
![Image](https://user-images.githubusercontent.com/86041345/215352081-520a58d6-e6a1-40a0-8b81-1ee431e530c3.png)
The URL above calls the `handleRequest` method, which takes said URL as an argument. This method calls `getPath` to
find the URL's path and calls `contains` to check if the path contains `"add-message"` (the argument of `contains`).
If so, `getQuery` is used to find the URL's query, and `split` is used to separate the query into two strings, based
on the left and right sides of the `"="` (the argument of `split`). These strings are saved in an array, `parameters`.

Next, `equals` is used to check if `parameters[0]` is equal to `"s"` (the argument of `equals`). If this is true, 
`"\n" + parameters[1]` is added to an ArrayList called `strings`, which tracks the messages added.

**Adding Another Message**
![Image](https://user-images.githubusercontent.com/86041345/215352161-ff36ff4a-b447-45f7-a58c-627039bad038.png)
