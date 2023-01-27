# Servers and Bugs
*by Matteo Persiani*

### Part 1
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-25%20at%207.40.40%20PM.png)
The code used to implement `StringServer`

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-25%20at%207.42.08%20PM.png)
* The handleRequest method is called for this command.
* Valid arguments include all letters, numbers, and sentences using these values. Certain symbols such as `=`, `#`, and other symbols, and spaces on their own produce errors. Go ahead and run the code yourself to see if you can find any other unique combinations that produce errors!
* Every time a valid new message is added, the `allAsString` variable changes and the `allInputs` ArrayList adds a value.

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-25%20at%207.42.30%20PM.png)
* The handleRequest method is called for this command.
* Valid argument for inputs after the first are the same as before.
* The same values are changed as before.

### Part 2
* A failure-inducing input for the buggy program:



```
@Test
public void averageWithoutLowestDupe() {
    double[] input = {0.5, 1.0, 2.0, 0.5};
    assertEquals(1.5, ArrayExamples.averageWithoutLowest(input), 0);
}
```



* An input that doesn’t induce a failure:


```
@Test
public void averageWithoutLowest() {
    double[] input = {1.0, 2.0, 0.5};
    assertEquals(1.5, ArrayExamples.averageWithoutLowest(input), 0);
}
```    
    
    
* The symptom:

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-25%20at%209.26.50%20PM.png)

* The code before the bug was fixed:


```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
        if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
        if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
}
```



* The code after the bug was fixed:


```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    int count = 0;
    double lowest = arr[0];
    for(double num: arr) {
        if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
        if(num != lowest) { 
        sum += num; 
        }
        else {
            count++;
        }
    }
    return sum / (arr.length - count);
}
```


* The fix addresses the issue by adding a `count` variable which keeps track of how many values of the lowest number there are and then subtracts this number from the array length to divide by the correct number of values that were added together

### Part 3

What I've learned: 
* In weeks 2 and 3 of lab I learned what the components of a URL are and each component does. I also learned how to run a server locally and remotely and how to write a code to take input from the URL to do some neat things. Lastly, I learned the what symptoms, bugs, and filure-inducing inputs are and the proper termonology to "correct" code.