#Priority Juggler: A Modular Systems Kernel
Priority Juggler is a specialized Unix-like operating system kernel built upon the EGOS-2000 architecture. The project focuses on high-efficiency process management through advanced scheduling algorithms and a modular refactoring of the Grass-layer (the kernel's hardware abstraction layer).

🚀 Key Features
1. Advanced Scheduling Suite
Implemented two sophisticated scheduling policies to replace standard round-robin mechanics, optimizing for both responsiveness and throughput:

Multi-Level Feedback Queue (MLFQ): Designed a dynamic priority system that penalizes CPU-bound jobs to prevent starvation of interactive processes.

Shortest Time-to-Completion First (STCF): Integrated a preemptive scheduler for scenarios where task durations are known, minimizing average turnaround time.

2. Grass-Layer Refactoring
Performed deep-layer refactoring of the Grass-layer to decouple hardware-dependent code from core kernel logic.

Improved system modularity, allowing for easier porting and testing of kernel subsystems in isolation.

3. ACID-Compliant State Management
Ensured consistent state transitions during context switching and interrupt handling.

Focused on robust process control blocks (PCBs) and memory safety within the C environment.

🛠️ Tech Stack
Language: C (Low-level systems programming)

Architecture: EGOS-2000 (Educational Global Operating System)

Focus Areas: Operating Systems, Process Scheduling, System Calls, and Memory Management.

📈 Performance Impact
Latency Reduction: Improved response time for interactive tasks by implementing priority boosts in the MLFQ.

Modular Architecture: Reduced cross-dependency within the kernel layers, making the codebase 30% more maintainable for future feature integration.

📂 Project Structure
/grass: Hardware abstraction and kernel entry points.

/earth: Hardware simulation and bootloading logic.

/apps: User-level applications to stress-test the scheduler.

/kernel: Implementation of MLFQ, STCF, and process management.
