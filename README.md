# Priority Queue Using Assembly Language

### CSE341 — Microprocessors Project | EMU8086

A priority-based task management system implemented in **8086 Assembly Language using EMU8086**. The project demonstrates how arrays, stack operations, macros, and procedures can be used to manage tasks according to their priority.

Unlike a standard FIFO queue, this system processes tasks with higher priorities first while maintaining the insertion order of tasks with equal priorities.

## Project Overview

The primary objective of this project is to implement a Priority Queue using low-level Assembly Language programming techniques.

Each task is assigned a unique identifier and an integer priority value. The system organizes tasks using an array and a stack-based approach to ensure that higher-priority tasks are processed before lower-priority ones.

The implementation focuses on priority comparison, task reordering, and efficient management of the queue using Assembly Language instructions.

## Key Features

- **Priority-Based Task Management:** Tasks are processed according to their assigned priorities.
- **Array-Based Storage:** Stores task identifiers and their corresponding priority values.
- **Stack-Based Organization:** Uses a stack-oriented approach to maintain task processing order.
- **Priority Comparison:** Compares task priorities to determine their positions.
- **Dynamic Reordering:** Adjusts task positions when new tasks are inserted.
- **Equal-Priority Handling:** Maintains FIFO order among tasks with identical priorities.
- **Macros and Procedures:** Organizes insertion, removal, and task-processing operations into reusable routines.

## Technologies Used

| Technology | Purpose |
|---|---|
| 8086 Assembly Language | Core programming language |
| EMU8086 | Assembly development and execution |
| Arrays | Task and priority storage |
| Stack Operations | Priority-based task organization |
| Macros | Reusable Assembly instructions |
| Procedures | Modular task management operations |

## System Design

The project consists of three main components.

### 1. Task Storage Using Arrays

Each task is represented by a unique identifier and an integer priority value.

The array structure maintains the information needed to compare and organize tasks.

### 2. Priority Management Using a Stack

A stack-based mechanism organizes tasks according to priority.

The intended processing order places the highest-priority task at the top. When a new task is added, the system compares priority values and adjusts the ordering accordingly.

### 3. Task Processing Using Macros and Procedures

Macros and procedures handle the main operations:

- Adding a new task
- Comparing task priorities
- Reordering tasks
- Removing the highest-priority task
- Managing tasks with equal priorities

## Example Workflow

Consider the following tasks:

| Task ID | Priority |
|---|---|
| T1 | 3 |
| T2 | 5 |
| T3 | 2 |
| T4 | 5 |

Assuming larger values represent higher priorities, the expected processing order is:

```text
T2 (5) → T4 (5) → T1 (3) → T3 (2)
```

Although T2 and T4 have equal priorities, T2 is processed first because it was inserted earlier.

This demonstrates both **priority-based ordering** and **FIFO handling for equal-priority tasks**.

## Algorithm

### Task Insertion

1. Accept a task identifier and its priority.
2. Store the task information.
3. Compare the new task's priority with existing tasks.
4. Reorder tasks according to their priorities.
5. Preserve insertion order when priorities are equal.

### Task Removal

1. Check whether the priority queue contains any tasks.
2. Identify the highest-priority task.
3. Remove that task.
4. Update the remaining task organization.

## How to Run

### Requirements

- EMU8086 Microprocessor Emulator
- Windows or a compatible environment capable of running EMU8086

### Execution

1. Open EMU8086.
2. Open the project's `.asm` source file.
3. Compile the Assembly program.
4. Run it using the emulator.
5. Observe the task insertion, priority organization, and removal operations.

## Learning Outcomes

This project demonstrates practical knowledge of:

- 8086 Assembly Language programming
- Priority Queue data structures
- Array and stack manipulation
- Processor registers and memory operations
- Conditional branching and priority comparisons
- Assembly macros and procedures
- Task scheduling principles
- FIFO ordering among equal-priority tasks

## Applications

Priority queues are relevant to:

- CPU and process scheduling
- Operating system task management
- Interrupt handling
- Network packet scheduling
- Real-time task processing

## Future Improvements

- Improve handling of queue overflow and underflow.
- Support more tasks and priority levels.
- Optimize task insertion and reordering.
- Implement an interactive task management interface.
- Compare the Assembly implementation with a high-level language version.

## Project Information

**Course:** CSE341  
**Project:** Priority Queue Using Assembly Language  
**Platform:** EMU8086  
**Language:** 8086 Assembly Language  
**Category:** Microprocessors / Data Structures / Low-Level Programming

## Note

This is an academic project developed to demonstrate priority-based task management using 8086 Assembly Language.
