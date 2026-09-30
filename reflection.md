# Stack Explorer Reflection

## 1. Stack Mechanics

This assignment helped me better understand what happens when a function is called and how the call stack works. Every time a function is called, a new stack frame is created to hold information such as local variables and where the program needs to return afterward. When I tested the factorial function, I could see how each recursive call added another level to the stack until it reached the base case. Once it reached that point, the functions started returning their results in reverse order.

The stack overflow demonstration showed why having a base case is important. Without one, the function keeps calling itself and creating more stack frames until the program eventually runs out of stack space. The safe recursion function fixed this by stopping once it reached a maximum depth of 10. I learned that recursion itself isn't necessarily dangerous, but it needs a stopping condition to prevent problems. Seeing the function calls printed in the terminal made it easier for me to understand something that was previously difficult to visualize.

## 2. Recursion Costs

One thing I noticed while testing Fibonacci was how quickly the number of function calls increased as I used larger values. I tested Fibonacci with 10, 20, and 30, and the maximum stack depths were 10, 20, and 30. Even though the depth increased gradually, the amount of repeated work grew much faster because the function kept calculating the same values multiple times.

This helped me understand why recursion isn't always the most efficient solution. Each function call uses stack memory, and repeated calculations can slow down a program. An iterative solution or memoization could make Fibonacci more efficient by avoiding unnecessary calculations.

## 3. Function Pointers and Callbacks

Before this assignment, I wasn't very familiar with function pointers or callbacks. I learned that a function pointer allows a program to reference a function and pass it to another function as an argument. In Part 4, I used callbacks to process the same array in different ways without rewriting the main processing function. The program doubled, squared, and negated the original array values.

In Part 5, I created an event system that registered three callbacks and triggered them using the value 100. This helped me understand how programs can respond to different events without having to know exactly what each callback will do beforehand. I can see how this would be useful in real applications, especially when handling button clicks, user input, or other events.