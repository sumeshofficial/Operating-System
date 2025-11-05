## Understanding Concurrency

Concurrency means performing multiple operations at the same time —
or more precisely, handling many tasks that overlap in time.

In a concurrent system, the Operating System (OS) allows multiple programs or threads to run together by sharing CPU time.
This makes your system faster and more responsive.

### The Problem with Concurrency

When multiple threads or processes try to access or modify the same data at the same time, problems can occur.
This happens because the CPU executes each operation in small steps, not all at once.

### Example: Bank Account Problem

Imagine two people sharing the same bank account.
The balance is ₹100.
Both people (threads) try to withdraw ₹50 at the same time.

| Step | Person A (Thread 1) | Person B (Thread 2) | Balance                                   |
| ---- | ------------------- | ------------------- | ----------------------------------------- |
| 1    | Reads ₹100          | —                   | ₹100                                      |
| 2    | —                   | Reads ₹100          | ₹100                                      |
| 3    | Subtracts ₹50 → ₹50 | Subtracts ₹50 → ₹50 | Both think balance = ₹50                  |
| 4    | Writes ₹50          | Writes ₹50          | Final balance = **₹50 ❌** (should be ₹0) |

### What Happened?

Both threads read the same old value (₹100) before either one updated it.
When they wrote the result back, one write overwrote the other’s work.
This is called a Race Condition —
when multiple threads “race” to access and change the same data.
