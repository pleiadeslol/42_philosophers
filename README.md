# Philosophers 🍝🤔💡

## Project Description

This project is a multi-threaded simulation of the classic dining philosophers problem, designed to explore the intricacies of concurrent programming and thread synchronization. 🧵🔒

## 🍽️ The Philosophical Dining Scenario

Imagine a round table with philosophers who alternate between three fundamental states:
- 🍴 Eating
- 💭 Thinking
- 😴 Sleeping

### 🔑 Key Constraints
- Philosophers sit around a table with a bowl of spaghetti
- Exactly one fork between each pair of philosophers
- A philosopher needs two forks to eat
- No communication between philosophers allowed
- Simulation ends if a philosopher dies of starvation

## 🖥️ Program Usage

```bash
./philo number_of_philosophers time_to_die time_to_eat time_to_sleep [number_of_times_each_philosopher_must_eat]
```

### 📋 Argument Breakdown
- `number_of_philosophers`: Total philosophers/forks (1-200)
- `time_to_die`: Maximum time (ms) before starvation
- `time_to_eat`: Time (ms) for eating
- `time_to_sleep`: Time (ms) for sleeping
- `number_of_times_each_philosopher_must_eat`: Optional simulation termination condition

## 🧩 Implementation Details

### 🧵 Threading Mechanics
- Each philosopher runs as a separate thread
- Forks protected by mutexes to prevent race conditions
- Circular table arrangement with shared resources

## 📝 Logging Specifications

State changes logged in precise format:
```
timestamp_in_ms philosopher_number state
```

Possible states include:
- 🥄 has taken a fork
- 🍝 is eating
- 💤 is sleeping
- 🤔 is thinking
- 💀 died

## 🛠️ Compilation Instructions

Utilize the provided Makefile:
```bash
make        # Compile project
make clean  # Remove object files
make fclean # Remove executable and object files
make re     # Recompile
```

### 🚩 Compilation Flags
- `-Wall`
- `-Wextra`
- `-Werror`

## 🧠 Learning Objectives
- Multi-threading fundamentals
- Mutex synchronization techniques
- Deadlock prevention strategies
- Concurrent resource management
- Precise timing in parallel programming

## ⚠️ Critical Requirements
- No global variables
- Strict memory management
- Zero memory leaks
- Philosophers must survive!

## 🛠 System Requirements
- C compiler (gcc/cc)
- POSIX threads library (pthread)

## 🚧 Potential Challenges
- Preventing deadlock scenarios
- Ensuring fair resource allocation
- Managing thread synchronization
- Implementing accurate timing mechanisms

## 💡 Pro Tips
- Test extensively with different philosopher counts
- Monitor thread interactions carefully
- Use debug logging for complex scenarios
- Validate all edge cases