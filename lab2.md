# Lab Report 2
## Part 1: StringServer
* Below is the code for the StringServer.java file that I used to create the StringServer web server:
![Image](THECODE.png)
* Now, here are two screenshots of using `/add-message` followed by a query:
![Image](SCServer1.png)
* Before this, the main method was called to start the server. This main method was called during the terminal, with an array of String `args` as an argument. The `port` field is specified to be the first element in `args` (ie the first argument when running StringServer).  In this main method, we call the `Server.start` method, where a new Handler object is created and passed as an argument alongside the `port` field. 
* Secondly, using the new Handler object that was created, this screenshot shows the `handleRequest` method of my code being called. 
* The URL is passed to the `handleRequest` method as an argument (`url`), and in that way the method can compile and run `url.getPath()` to get the path of the localhost URL.
* My code specifies if no path is mentioned in the URL, return nothing, and for paths that contained `/add-message`, it should get the query and add the query part after the `=` sign to the string that we want to show. 
* The `toShow` field which is a part of the Handler class exists and maintains as long as the server is running because it is a field from the same Handler object that was created. So, as we call `handleRequest` by using the `/add-message` path in our localhost, we continually add to whatever `toShow` currently is, meaning we append to the value of `toShow` with this request, able to constantly change its value.
* The `queryParam` field is defined as `url.getQuery().split("=");`, and so it is whatever query was specified in the URL, changing depending on whatever the URL is at the moment.

![Image](SCServer2.png)
* The main method here is not called at it has already been called. Calling the main method again would restart the server and make a new Handler object, erasing memory of the toShow field by setting it back to an emtpy String.
* However, here, the `handleRequest` method here is indeed called once again because a new URL has been entered - this time with a different value specified by `/add-message`. Now, the `url` argument that is passed into the `handleRequest` method has changed, and so the value of the `queryParam` field changes accordingly as well. Thus, due to all of this, the `toShow` field retains its value from the last screenshot but now also adds onto the previous String value with the new query parameter that was specified.
## Part 2: Assessing bugs using JUnit
* Below is a failure inducing input for the for the `averagewithoutLowest` method. The input is formatted as a JUnit test method:
```@Test
  public void testAverageWithoutLowest(){
    double[] input = {1,1,1,3,4,5};
    assertEquals(12,ArrayExamples.averageWithoutLowest(input),0.00001);
  }
```

