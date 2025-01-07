# **Advanced Process Management**

## **Process**
- Code in the execution state is called a **process**.
- It is an instance of a program in execution.

### **States of a Process**:
1. **Running**
2. **Stopped**
3. **Idle**
4. **Zombie**
5. **Orphan** *(Frequently asked in interviews)*
6. **Sleep**

### **Types of Processes**:
1. **Batched**
2. **Real-Time**
3. **Daemon**
4. **Interactive**

---

## **Threads**
- A thread is a unit of a single process.
- **Key Characteristics**:
  - Multiple threads can exist inside a single process.
  - All threads share the same resources allocated to the process.
  - A process has a dedicated resource limit from the available system resources.
  - **Bash scripts** typically use the `.bash.sh` extension.

---

### **Feature Comparison: Process vs. Thread**

| **Feature**       | **Process**            | **Thread**             |
|--------------------|------------------------|------------------------|
| **Memory Space**   | Has its own RAM        | Shares memory with other threads of the same process |
| **Creation Time**  | More time             | Less time              |

---

## **Real-Life Examples**
- Payment Gateway
- Webserver Handling Traffic
- Infrastructure Provisioning
- CI/CD Pipeline Optimization
- Linux Scripts
- Monitoring
- Containerization
- Microservices Architecture

---

## **Concurrency vs. Parallelism**

### **Concurrency**: *Multitasking*
- Handles multiple tasks or operations simultaneously.
- Example: 
  - While water is boiling, chop vegetables.
  - While noodles are cooking, prepare the masala mix.
  - One person multitasks between different activities.

### **Parallelism**: *Simultaneous Execution*
- Every task is taken care of by a different person or entity.
- Example:
  - Person 1 boils water.
  - Person 2 chops vegetables.
  - Person 3 prepares the masala mix.
  - Multiple people work simultaneously on different tasks.

### **Key Difference**:
| **Aspect**         | **Concurrency**                     | **Parallelism**                     |
|---------------------|-------------------------------------|-------------------------------------|
| **Execution**       | Single person switching tasks       | Multiple people working on tasks    |
| **Best Scenario**   | Useful when there’s a wait time     | Useful for tasks that can run independently |

### **Parallelism Complements Concurrency**
- Both concepts can be applied depending on the scenario:
  - Use **parallelism** when tasks are independent and can run simultaneously.
  - Use **concurrency** when tasks involve significant wait times.

---

## **CI/CD Pipeline Optimization**

### **Typical Steps**:
1. **Git Clone**
2. **Lint Test**
3. **Code Coverage**
4. **Unit Test**
5. **Security Test**
6. **Build Step**
7. **Create Docker Image**
8. **Push Image to Container Repo**

- **Current Approach**: These steps happen concurrently, taking ~30 minutes to complete.
- **Optimization**: Testing steps can be executed in parallel to reduce overall completion time.
