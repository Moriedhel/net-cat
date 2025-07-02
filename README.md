# Push-Swap

## 🧩 Project Description

**Push-Swap** is a sorting project that uses a *non-comparative sorting algorithm* and a custom instruction set. The goal is to sort a list of integers with the minimum number of operations using only two stacks and a restricted set of commands.

This project consists of two programs:

- `push-swap`: Generates and outputs the minimal list of operations to sort the stack.
- `checker`: Validates a list of instructions to verify whether the stack is correctly sorted.

## 📜 Stack Rules & Instructions

The sorting algorithm works with two stacks: `a` (initially filled with values) and `b` (initially empty).

### Available Instructions:

| Command | Description |
|---------|-------------|
| `sa`    | Swap the first 2 elements of stack a |
| `sb`    | Swap the first 2 elements of stack b |
| `ss`    | Execute `sa` and `sb` |
| `pa`    | Push the first element from stack b to stack a |
| `pb`    | Push the first element from stack a to stack b |
| `ra`    | Rotate stack a (first element becomes last) |
| `rb`    | Rotate stack b |
| `rr`    | Execute `ra` and `rb` |
| `rra`   | Reverse rotate stack a (last element becomes first) |
| `rrb`   | Reverse rotate stack b |
| `rrr`   | Execute `rra` and `rrb` |

## 🚀 Usage

### ✅ push-swap

Generates and outputs the shortest sequence of instructions to sort the input.

```bash
$ ./push-swap "2 1 3 6 5 8"
pb
pb
ra
sa
rrr
pa
pa
