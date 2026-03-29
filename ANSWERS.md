# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?
A process is a BIG program with its own memory and resources, while a thread is a smaller unit inside a process that shares the same memory space. Threads are smailer and faster to create because they do not need separate memory like processes do. In this assignment, we used threads because they allow multiple tasks to run at same time without the  overhead of creating new processes. Threads are more suitable for simulations like this because they make the system faster and more efficient.
]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[in Round-Robin, when a process not finish in the time quantum, it go back to the end of the ready queue. It wait there until all other processes get their turn, then it run again later. In my output, P1 use 3000ms but still have 1968ms left, so the scheduler put it back in the queue. This show that the process keep coming back until it finish completely
]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [P1 is in New state when the program first create the thread object, before it go inside the ready queue or start running.
]

2. **Runnable**: [P1 become Runnable when the scheduler add it to the ready queue at the start of the simulation, meaning it is ready to run but not running yet.
]

3. **Running**: [P1 enter Running state when the CPU give it the time quantum and it start using the 3000ms slice, doing its burst work
]

4. **Waiting**: [P1 go to Waiting after it finish the quantum but still have remaining time, so it wait in the ready queue for next turn while other processes run.
]

5. **Terminated**: [P1 become Terminated when it finish all its burst time and no more CPU work is needed, so the thread stop completely.
]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [ Online Game]

**Description**: 
[In online game, many players well play in the same time, like move, jump, The game need to gave  every player fast and fair gamepaly so no player get delay or freez.
]

**Why Round-Robin works well here**: 
[Round‑Robin give each player small time slice to process their action, so all players get equal chance and game be smooth and fair]

### Example 2: [Online Store ]

**Description**: 
[In online store, many customers open pages, and buy items, and checkout at same time. The server need handle every customer  fast so the website not slow or crash.]

**Why Round-Robin works well here**: 
[Round‑Robin give each customer request small time slice, so all users get good service and no one wait too long or freez]

---

## Summary

**Key concepts I understood through these questions:**
1. I understood how Round‑Robin give fair time slice to every thread so no thread wait too long.
2. difference between thread and process, and how thread is lighter and faster because it share memory inside same program.
3. how round-robin work in real world

**Concepts I need to study more:**
1. how thread work in program
2.  difference between thread and process, and how thread is lighter and faster because it share memory inside same program.
