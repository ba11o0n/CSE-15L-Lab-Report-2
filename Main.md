# Lab Report 2 
## **String Server Code:**
<img src="L2_Code.png" width="600" height="300"/>

### **Examples** 
<img src="L2_s1.png" width="800" height="500"/>

## **Part 2: A Bug** 
#### The code snippet from lab 3. 
```java
public class ArrayExamples{
   static void reverseInPlace(int[] arr){
      for(int i = 0; i < arr.length; i += 1){
      arr[i] = arr[arr.length - i - 1]; 
      }
   }
}
```

#### An input that doesn’t induce a failure, as a JUnit test and any associated code
```java
int[] input1 = { 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input1); 
```

#### A failure-inducing input 
```java
int[] input2 = {1, 2, 3};
ArrayExamples.reverseInPlace(input2);
assertArrayEquals(new int[]{2, 2, 1}, input2); 
```
<img src="fail.png" width="500" height="300"/>
