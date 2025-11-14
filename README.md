# 🥢 Philosophers  
**A simulation of the Dining Philosophers problem using C and POSIX threads.**

![C](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge)
![Threads](https://img.shields.io/badge/Concurrency-Pthreads-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

---

## 📌 Overview  
**Philosophers** simulates the classic **Dining Philosophers problem** using threads.  
It demonstrates proper **thread synchronization** to prevent deadlocks and race conditions while managing philosopher actions: thinking, eating, and sleeping.

Key focuses of the project:  
- Thread creation and management using `pthread`  
- Mutex synchronization for forks  
- Timed actions and monitoring  
- Safe resource sharing among threads  

---

## ✨ Features  
- ✅ Correct simulation of multiple philosophers  
- ✅ Deadlock avoidance  
- ✅ Mutex-protected forks  
- ✅ Time-based actions (eat, sleep, think)  
- ✅ Configurable simulation via command-line parameters  

---

## 🗂 Project Structure  
```
philosophers/
│── creat_threads.c      # Thread creation
│── dead_monitor.c       # Monitors philosopher deaths
│── init.c               # Initialization routines
│── main.c               # Program entry point
│── philo_actions.c      # Philosopher actions
│── philo_routine.c      # Philosopher main routine
│── print.c              # Printing state messages
│── time.c               # Timing utilities
│── utils.c              # Helper functions
│── philo.h              # Header file
│── Makefile             # Build instructions
└── README.md
```

---

## 🚀 Installation

### 1️⃣ Clone the repository  
```bash
git clone https://github.com/yourusername/philosophers.git
cd philosophers
```

### 2️⃣ Build the project  
```bash
make
```

> The Makefile generates the `philo` executable.

---

## ▶️ Usage

### Run the simulation  
```bash
./philo <number_of_philosophers> <time_to_die> <time_to_eat> <time_to_sleep> [number_of_meals]
```

- `<number_of_philosophers>` – Total philosophers  
- `<time_to_die>` – Time in milliseconds before a philosopher dies if not eating  
- `<time_to_eat>` – Time in milliseconds to eat  
- `<time_to_sleep>` – Time in milliseconds to sleep  
- `[number_of_meals]` *(optional)* – Number of times each philosopher must eat  

---

> Example: Terminal output showing philosopher states in real time.

---

## 🧹 Cleanup  

Remove compiled binaries:  
```bash
make fclean
```

---

## 📄 License  
This project is licensed under the **MIT License**.
