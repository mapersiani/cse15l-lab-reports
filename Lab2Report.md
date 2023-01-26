# Servers and Bugs
*by Matteo Persiani*

### Part 1
![Image]()
![Image]()
* The handleRequest method is called for this command
* 
![Image]()
* The handleRequest method is called for this command

### Part 2
* A failure-inducing input for the buggy program:


    @Test
    public void averageWithoutLowestDupe() {
        double[] input = {0.5, 1.0, 2.0, 0.5};
        assertEquals(1.5, ArrayExamples.averageWithoutLowest(input), 0);
    }

* An input that doesn’t induce a failure:


    @Test
    public void averageWithoutLowest() {
        double[] input = {1.0, 2.0, 0.5};
        assertEquals(1.5, ArrayExamples.averageWithoutLowest(input), 0);
    }
    
* The symptom:
![Image]()

* The code before the bug was fixed:


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

* The code after the bug was fixed:


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
### Part 3

What I've learned: 