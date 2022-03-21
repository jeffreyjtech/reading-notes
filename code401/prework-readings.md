# Prework - Miscellaneous Readings and Videos

## Solving Problems

In this article, the author explains a set of steps to solve algorithm-type programming problems, and then goes on to explain each step in detail. To summarize the article, the 6 steps are:

1. Read the problem completely twice: You must understand a problem to solve it, plain and simple.
2. Solve the problem manually with 3 sets of sample data: To me this means to solve the problem in the most simple stupid way, creating a "word solution" to the word problem, and do preliminary tests of your solution.
3. Optimize the manual steps: Use more advanced tools, constructs, and techniques to improve the manual solution you just made.
4. Write the manual steps as comments or psuedo-code: A great idea and a critical step if you weren't working with code in the previous steps, which I personally prefer to do.
5. Replace the comments or psuedo-code with real code: Again, critical step if you wrote out pseudo-code or comments to translate the solution to real code.
6. Optimize the real code: Improve the real code just written with appropriately descriptive variable names and DRY-ify it.

## Act like you make $1000/hr

[Error 410. The author deleted this Medium story.](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)

## How to think like a programmer

This article is similar to **Solving Problems**. It's important to have a framework for problem-solving. The author lays a 4-step framework for solving coding problems, which is in opposition just to trying solutions without forethought or reflection.

1. Understand the problem: Again, you can't really solve a problem that you don't understand. Get to the level of understanding that you can explain it in plain English and/or make a diagram of it.
2. Plan your solution: Use pseudo-code or comments to write out a "blueprint" of the process.
3. Divide: Break down the problem into sub-problems, and solve each one-by-one, generally starting with the simplest one.
4. Things to do when you're stuck:
    - Debug: Go through your code step by step with a debugger to examine if you're assumptions about how the code should be written is actually what you needed to write.
    - Reassess: Take a step back and look at the problem from another angle. Find ways to de-tangle any complicated aspects of the solution into something more generalized.
    - Google: When all else fails, a Google search can help you find useful code snippets to solve a sub-problem. It's **not** recommended to search for the solution to the whole problem.

Beyond this framework, it's important to practice problem-solving. The author goes so far as to recommend you make a hobby out of problem-solving in your off-time with games, puzzles, and other problem-solving-like activities.

I'm sure it's effective, but this is misguided advice in my opinion. Unless you're absolutely determined to be a rockstar programmer, or enjoy problem-solving for its own sake, you ought to do what makes you happy in your free time.

## The 5 Whys

The 5 Why's is a problem-solving method developed by Sakichi Toyoda, founder of Toyota Industries. Essentially, when you find a problem you'll generally get to the true root cause after asking "Why is this happening?", then asking "Why?" again about the answer to the 1st question.

These are the steps for applying the 5 Why's method:

1. Assemble a Team: Using the 5 Why's method is best done when you have assembled a team of stakeholders who have hands-on knowledge of the issue and a facilitator to act as the "project lead".
2. Define the problem: Observe the problem in action and create a definition/problem statement that the whole team agrees on.
3. Ask the first "Why?": Ask "Why is this problem occurring?". That's the idea at least. Get a single, serious answer grounded in reality.
4. Ask "Why?" 4 more times: Use the "Why?" question to drill deeper into the first-level cause, and then the second-level cause and so on. This can be a one-way process, or branch off into lanes to follow multiple contributing factors when appropriate to best answer a "Why?
5. Know when to stop: It should readily apparent when you've happened upon a root cause, because there will be no more useful responses to be had by asking "Why?" questions. Either that or you've reached the limit of your team's zone of control for a problem. Craft the most complete solution you can with the information gathered in the previous steps. If you still don't fully understand the problem, use a different problem-solving technique.

## What the heck is the event loop anyway?

I found this to be super interesting so I wrote a lot.

- The Chrome JavaScript V8 runtime has a heap of allocated memory and a stack of execution contexts
- There are many "built-in" WebAPIs which the V8 runtime uses to provide various features, such as DOM manipulation, ajax, and some asynchronous methods.
- The V8 runtime utilizes the above features AND an event loop and a callback queue of callback functions to execute JavaScript.
- JavaScript is a single-threaded language: it can execute only one thing at a time from it's singular callstack. The callstack is basically just the list of functions which the runtime is executing inside of at the current moment.
  - When a JS runtime invokes a function inside of a function, the 1st function is already in the callstack, and the 2nd function is added to the top of the stack.
- JavaScript uses asynchronous callback functions to perform work asynchronously. When us programmers tell JS to execute something which will take time, we define a callback function which will be invoked when that "long-term" task is finished. In the meantime, the callstack is freed up to execute other code. This feature of JS absolutely critical for a good user experience on a web application which can't just lock up every time it makes a network request.
- Web browsers, NOT the JS runtime alone, provide the tools for multi-threaded execution. The WebAPIs executes tasks separately from the runtime, in the background.
- When the WebAPIs are finished, the callback functions we gave to them are added onto the task queue.
- When the runtime callstack is clear (it could have been executing main() or an async stack), the event loop removes a single callback function from the task queue (FIFO) and places them into the runtime callstack.

## The Super Mario Effect

The Super Mario Effect is to game-ify tasks in order to learn more and persevere when you want to accomplish something. Game-ifying a task means reframing it to make it more engaging and accepting failure as an option. Game-ifying a project means focusing on the long-term goal of the project instead of fixating on the trials and tribulations you've encountered or foresee. This way you can appreciate the journey rather than giving up. You sidestep the feeling that you're losing something when you fail and instead appreciate the knowledge you've gained from failing.
