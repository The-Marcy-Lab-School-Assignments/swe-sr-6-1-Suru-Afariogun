# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

The process of providing only the essentials and hiding the details is known as abstraction.
An Abstract Data Type (ADT) is a conceptual model that defines a set of operations and behaviors for a data structure. ADTs operate by defining what operations are possible without detailing their implementation or how data is oganized in memeory. Learning ADTs and how they function can help engineers design and conceptualize data structures and have a way of encapsulating data and operations on that data into a single unit. With ADT's you get Encapsulation, Abstraction, Data Structure Independence, Information Hiding, and Modularity. Overall, ADTs provide a powerful tool for organizing and manipulating data in a structured and efficient manner.

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4

A palidrome is a word, phrase, or sequence that reads the same backward as forward, e.g., madam or nurses run. Below I am using a stack to identify if an inputed string is an palidrome:

```Javascript
function isPalindrome(str)
{
    let length = str.length;

    // Creating a Stack
    let stack = [];

    // Finding the middle
    let  mid = str.length / 2;

    for (i = 0; i < mid; i++) {
        stack.push(str[i]);
    }

    // Checking if the length of the string
    // is odd, if odd then neglect the
    // middle character
    if (length % 2 != 0) {
        i++;
    }

    let char = null;
    // While not the end of the string
    while (i != str.length)
    {
         char = str[str.length-1];
         str.pop();

    // If the characters differ then the
    // given string is not a palindrome
    if (char != str[i])
        return false;
        i++;
    }

return true;
}
```

First you must get the length of the string. Now, find the character in the middle of the string.
Push all the characters from begining to middle of the string into a stack.
If the length of the string is odd then neglect the middle character.
Until the end of the string is met, keep popping elements from the stack as you iterate through the string, and compare them with the current character. If there is a mismatch then the string is not a palindrome. If all the elements match then the string is a palindrome.
