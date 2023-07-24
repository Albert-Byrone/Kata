_**1. Define a function that removes duplicates from an array of non negative numbers and returns it as a result.**_
### BDD:

Feature: Remove Duplicates from Array

   _As a user
    I want to remove duplicate elements from an array of non-negative numbers
   So that I can get a unique sequence in the same order_

Scenario 1 : Removing duplicates from an array

    Given an array of non-negative numbers: [5, 2, 7, 2, 1, 5, 9]
    When I call the removeDuplicates function
    Then the result should be: [5, 2, 7, 1, 9]

Scenario 2 : Array with no duplicates

    Given an array of non-negative numbers with no duplicates: [1, 3, 6, 2, 9]
    When I call the removeDuplicates function
    Then the result should be the same array: [1, 3, 6, 2, 9]

Scenario 3 : Array with only one element

    Given an array with a single non-negative number: [4]
    When I call the removeDuplicates function
    Then the result should be the same array: [4]

Scenario 4 : Empty array

    Given an empty array: []
    When I call the removeDuplicates function
    Then the result should be an empty array: []

### Pseudocode

1. Create a function called  removeDuplicates which takes an array arr as input.
2. Initialize an empty array called uniqueElements to store the unique elements.
3. Iterate through each element in the input array arr. 
4. For each element, check if it is not already present in the uniqueElements array. 
5. If the element is not in the uniqueElements array,append it to the array. 
6. After iterating through all elements in the input array, I have collected all unique elements in the uniqueElements array. 
7. Finally, return the uniqueElements array, which contains the non-duplicate elements in the same order as they appear in the input array.


### Code Example:
  ```
function removeDuplicates(arr) {
   // Create an empty array to store the unique elements
  const uniqueElements = [];

   // Loop through each element in the input array
  for (const element of arr) {
     // Check if the element is not already in the uniqueElements array
    if (!uniqueElements.includes(element)) {
       // If it's not in the array, add it to the uniqueElements array
      uniqueElements.push(element);
    }
  }
   // return the array with duplicates removed
  return uniqueElements;
}
  ```
