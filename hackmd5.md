---
canonical_url: https://www.scaler.com/topics/deterministic-and-non-deterministic-algorithm/
title: Deterministic and Non-Deterministic Algorithms - Scaler Topics
description: With this article by Scaler Topics we will learn about the Difference Between Deterministic and Non-Deterministic Algorithms along with their examples and explanations.
category: DSA
author: Mansi
---

:::section{.abstract}

## Overview
An algorithm is a group of clearly defined steps used in programming to carry out certain tasks and produce desired results. When we refer to "a set of defined instructions" in this context, we mean that the user is aware of the results of those instructions if they are carried out as intended.

Deterministic and Non-deterministic Algorithms are two different types of algorithms based on the knowledge of the results of the instructions. Learn more about deterministic and non-deterministic algorithms in this article by Scaler Topics and how they differ.

:::
:::section{.abstract}

## Deterministic Algorithm

An algorithm is said to be deterministic if each algorithm's output has a distinct definition. So, a deterministic algorithm always finishes with an accept or refuse state and the same outcome after a predetermined number of steps. The same instruction is run on the target machine, which produces identical results regardless of how or how the instruction is performed.

A problem can be solved using deterministic algorithms in polynomial time. Deterministic algorithms always produce the same output, regardless of the input they are given. A common example of a deterministic algorithm is a mathematical function.

A deterministic algorithm is an algorithm that, given the same input and initial conditions, will always produce the same output and follow the same sequence of steps. Here's an example of a deterministic algorithm:

**Example: Finding the Maximum Number in an Array**

```javascript
function findMaximum(arr) {
  if (arr.length === 0) {
    // Handle the case of an empty array
    return undefined;
  }

  let max = arr[0]; // Initialize the maximum to the first element

  for (let i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i]; // Update the maximum if a larger element is found
    }
  }

  return max; // Return the maximum value
}

const numbers = [12, 45, 67, 23, 98, 56, 34];
const maxNumber = findMaximum(numbers);
console.log("The maximum number is:", maxNumber);
```

In this example, the `findMaximum` function takes an array of numbers as input and determines the maximum number in the array. It follows a deterministic algorithm because, for the same input array, it will always produce the same result. The algorithm initializes the maximum to the first element, iterates through the array, and updates the maximum whenever it encounters a larger number.

No matter how many times you run this algorithm with the same input (the `numbers` array in this case), it will consistently return the same maximum value, making it a deterministic algorithm.

:::
:::section{.main}

## Non Deterministic Algorithm
A non-deterministic algorithm is one in which no algorithm's output is uniquely determined, leaving the possibility of a random outcome. The non-deterministic algorithms have various results as a result.

Since non-deterministic algorithms might follow many different pathways to completion, predicting the machine's subsequent state is quite challenging. A non-deterministic algorithm cannot solve a problem in polynomial time, in contrast to deterministic algorithms. Examples of nondeterministic algorithms include random functions.

A non-deterministic algorithm is an algorithm in which the output or behavior is not uniquely determined by its input and execution steps. Instead, it may have multiple possible outcomes, and you cannot predict with certainty which one will occur. Non-deterministic algorithms are often used in theoretical computer science and are associated with non-deterministic Turing machines.

One classic example of a non-deterministic algorithm is the **non-deterministic finite automaton (NFA)** used in regular language recognition. NFAs are a type of automaton used to recognize regular languages (languages that can be defined using regular expressions). Unlike deterministic finite automata (DFAs), NFAs can have multiple possible transitions for a given input symbol and current state.

Here's a simplified example of an NFA that recognizes strings over the alphabet `{0, 1}` that end with "`01`" or "`10`":

```plaintext
State 0 --(0/ε)--> State 1 --(1/ε)--> State 2 (Accept)
  \                  /
   --(1/ε)-----------/
```

In this NFA:

- There are three states: State `0`, State `1, and State `2`.
- The transitions labeled with "0/ε" and "1/ε" indicate that when the input is "`0`" or "`1`," the NFA can choose to either transition to another state (non-deterministic choice) or consume no input (ε represents an empty transition).
- The double line from State `1` to State `2` represents an accepting state, meaning that if the NFA reaches State `2`, it accepts the input string.

For example, if you input the string "`001`", the NFA can choose to transition from State `0` to State `1` (using "`0/ε`"), then from State `1` to State `2` (using "1/ε"). Thus, it accepts the input.

Non-deterministic algorithms like NFAs have theoretical significance in computer science and formal language theory. They demonstrate that non-determinism can lead to more concise and expressive ways of specifying certain types of languages and problems, even though the precise execution path may not be determined by the input.

:::
:::section{.main}

## Difference between Deterministic and Non Deterministic Algorithm

The primary distinctions between deterministic and non-deterministic algorithms are as follows.

| Key    Aspect             | Deterministic Algorithm                               | Non-deterministic Algorithm                       |
|:---------------------:|:-----------------------------------------------------:|:---------------------------------------------------:|
| **Definition**          | Deterministic algorithms produce uniquely defined results. They perform a fixed number of steps and always finish with an accept or reject state with the same result. | Non-deterministic algorithms do not produce uniquely defined results. The outcome may be random or not uniquely determined. |
| **Execution**           | In deterministic algorithms, the target machine executes the same instructions and yields the same outcome, independent of the way or process of execution. | In non-deterministic algorithms, the machine executing each operation can choose any of several outcomes, subject to a determination condition defined later. |
| **Type**                | Deterministic algorithms are classified as reliable algorithms. They consistently produce the same output for the same input instructions. | Non-deterministic algorithms are considered non-reliable algorithms because they may produce different outputs for the same input. |
| **Execution Time**      | Deterministic algorithms typically execute in polynomial time since the outcome is known and consistent across executions. | Non-deterministic algorithms often cannot be executed in polynomial time due to their unpredictable nature. |
| **Execution Path**      | In deterministic algorithms, the execution path remains the same in every execution. | In non-deterministic algorithms, the execution path varies between executions and may take different, random paths. |

:::
:::section{.faq-section}

## FAQs 

Q. **Can you provide an example of a deterministic algorithm?**

A. An example of a deterministic algorithm is binary search. Given a sorted list, binary search follows a fixed process to find a specific element, and it always produces the same result for the same input.

Q. **What are some characteristics of deterministic algorithms?**

A. Deterministic algorithms are predictable, repeatable, and produce the same result for the same input. They are typically used when consistency and reliability of results are essential.

Q. **When are non-deterministic algorithms used?**

A. Non-deterministic algorithms are often used in scenarios where randomness, choices, or exploring multiple possibilities are required. Examples include randomized algorithms and some optimization problems.

:::
:::section{.summary}

## Conclusion 

* **Deterministic algorithms** guarantee consistent results for the same input, providing reliability and predictability.
* **Non-deterministic algorithms** introduce randomness, which can be beneficial in areas like randomized optimization and cryptography.
* **Deterministic algorithms** are easier to design, analyze, and debug due to their predictable behavior.
* **Non-deterministic algorithms** require probabilistic analysis and can provide efficient solutions in certain scenarios.
* The choice between them depends on the problem and the trade-offs between determinism and efficiency.
* Often, a combination of both deterministic and non-deterministic algorithms is used for optimal results, offering reliability and speed where needed.

:::

<!-- ## MCQs 
Question 1: What is a Deterministic Algorithm?
A) An algorithm that produces random results
B) An algorithm with unpredictable behavior
C) An algorithm that consistently produces the same result for the same input
D) An algorithm that always accepts any input

Answer: C) An algorithm that consistently produces the same result for the same input

Question 2: Which of the following best describes Non-Deterministic Algorithms?
A) Algorithms that execute in constant time
B) Algorithms that always produce correct results
C) Algorithms that may have multiple possible outcomes for the same input
D) Algorithms that never terminate

Answer: C) Algorithms that may have multiple possible outcomes for the same input

Question 3: In a Deterministic Algorithm, the result is:
A) Random
B) Consistently the same for the same input
C) Unpredictable
D) Dependent on the computer's processing speed

Answer: B) Consistently the same for the same input -->