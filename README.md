# CodeChallenges

Challange #1

Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.

Example

For inputArray = [3, 6, -2, -5, 7, 3], the output should be
adjacentElementsProduct(inputArray) = 21.

7 and 3 produce the largest product.

func adjacentElementsProduct(inputArray: [Int]) -> Int {
   var holdingArray: [Int] = []
   let count = inputArray.count
   var i = 0 
   var maxNum = 0 
   -----------------------
   while i < count - 1 {
       holdingArray.append(inputArray[i] * inputArray[i + 1])
       i = i + 1 
       maxNum = holdingArray.max() ?? 0
   }
   return maxNum
}
 -----------------------

Challange #2

Below we will define an n-interesting polygon. Your task is to find the area of a polygon for a given n.

A 1-interesting polygon is just a square with a side of length 1. An n-interesting polygon is obtained by taking the n - 1-interesting polygon and appending 1-interesting polygons to its rim, side by side. You can see the 1-, 2-, 3- and 4-interesting polygons in the picture below.

func shapeArea(n: Int) -> Int {
  var area: Int 
  if n != 0 {
      area = ((n - 1) * 2 * n) + 1
      print(area)
      return area
  }
   return n
}
 -----------------------

Challange #3

Ratiorg got statues of different sizes as a present from CodeMaster for his birthday, each statue having an non-negative integer size. Since he likes to make things perfect, he wants to arrange them from smallest to largest so that each statue will be bigger than the previous one exactly by 1. He may need some additional statues to be able to accomplish that. Help him figure out the minimum number of additional statues needed.


func makeArrayConsecutive2(statues: [Int]) -> Int {
   var output = 0 
   var maxNum = statues.max() ?? 0 
   var minNum = statues.min() ?? 0 
   var count = statues.count ?? 0 
   
   output = maxNum - minNum - count + 1 
   
        /*
        
        the comments here show a diffrent train of thought for getting the correct output 
        back but it would fail do to the fact it would take to long to get the test to pass
        I do keep return output at the bottom however since there was no need to change the variable name 
        
        */
//    var sorted = statues.sorted()
//    let amount = sorted.count
//    for count in 0...amount   {
//        while sorted[count] + 1  != sorted[count  + 1]  {
//            print("we are in the while loop")
//            sorted.append(sorted[count] + 1)
//            output += 1  
//            print("output is \(output)")
//            sorted = sorted.sorted()
//            print(sorted)
       
//        } 
//    }
//    print(output)
//    print("this is going to fail")
   return output
   
}
