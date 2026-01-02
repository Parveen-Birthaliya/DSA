# Infosys Technical MCQs - DBMS, OOP, OS, Networks

## 📚 Section 1: Database Management Systems (DBMS)

### **Key Concepts:**

#### **Normalization:**
- **1NF:** No repeating groups, atomic values
- **2NF:** 1NF + No partial dependency
- **3NF:** 2NF + No transitive dependency
- **BCNF:** 3NF + Every determinant is a candidate key

#### **Keys:**
- **Primary Key:** Unique identifier
- **Foreign Key:** References primary key of another table
- **Candidate Key:** Can be primary key
- **Super Key:** Set of attributes that uniquely identifies
- **Composite Key:** Multiple attributes as key

#### **Joins:**
- **INNER JOIN:** Matching rows from both tables
- **LEFT JOIN:** All from left + matching from right
- **RIGHT JOIN:** All from right + matching from left
- **FULL OUTER JOIN:** All rows from both

---

### **DBMS MCQs (30 Questions):**

**1.** Which normal form eliminates partial dependency?
- A) 1NF  B) 2NF  C) 3NF  D) BCNF
<details><summary>Answer</summary>B) 2NF</details>

**2.** What does ACID stand for in DBMS?
- A) Atomicity, Consistency, Isolation, Durability
- B) Accuracy, Consistency, Integrity, Durability
- C) Atomicity, Continuity, Isolation, Durability
- D) None
<details><summary>Answer</summary>A) Atomicity, Consistency, Isolation, Durability</details>

**3.** Which SQL command is used to remove a table?
- A) DELETE  B) REMOVE  C) DROP  D) TRUNCATE
<details><summary>Answer</summary>C) DROP</details>

**4.** What is the result of `SELECT COUNT(*) FROM employees WHERE salary > 50000;`?
- A) Sum of salaries  B) Number of employees with salary > 50000
- C) Average salary  D) Maximum salary
<details><summary>Answer</summary>B) Number of employees with salary > 50000</details>

**5.** Which keyword is used to sort results in ascending order?
- A) SORT BY  B) ORDER BY  C) GROUP BY  D) ARRANGE
<details><summary>Answer</summary>B) ORDER BY</details>

**6.** What is the purpose of GROUP BY clause?
- A) To sort data  B) To group rows with same values
- C) To join tables  D) To filter data
<details><summary>Answer</summary>B) To group rows with same values</details>

**7.** Which constraint ensures a column cannot have NULL values?
- A) UNIQUE  B) CHECK  C) NOT NULL  D) PRIMARY KEY
<details><summary>Answer</summary>C) NOT NULL</details>

**8.** What does the HAVING clause do?
- A) Filters rows before grouping  B) Filters groups after GROUP BY
- C) Sorts results  D) Joins tables
<details><summary>Answer</summary>B) Filters groups after GROUP BY</details>

**9.** Which join returns all rows from left table?
- A) INNER JOIN  B) LEFT JOIN  C) RIGHT JOIN  D) FULL JOIN
<details><summary>Answer</summary>B) LEFT JOIN</details>

**10.** What is a foreign key?
- A) Unique identifier  B) References primary key of another table
- C) Can be NULL  D) Both B and C
<details><summary>Answer</summary>D) Both B and C</details>

**11.** Difference between DELETE and TRUNCATE?
- A) DELETE can be rolled back, TRUNCATE cannot
- B) TRUNCATE is faster
- C) DELETE can have WHERE clause
- D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**12.** Which is not a DDL command?
- A) CREATE  B) ALTER  C) DROP  D) SELECT
<details><summary>Answer</summary>D) SELECT (It's DML)</details>

**13.** What is a view in DBMS?
- A) Physical table  B) Virtual table based on query
- C) Index  D) Constraint
<details><summary>Answer</summary>B) Virtual table based on query</details>

**14.** Which clause is used with aggregate functions?
- A) WHERE  B) HAVING  C) ORDER BY  D) GROUP BY
<details><summary>Answer</summary>D) GROUP BY (and HAVING)</details>

**15.** What is the maximum number of primary keys in a table?
- A) 1  B) 2  C) Unlimited  D) Depends on columns
<details><summary>Answer</summary>A) 1</details>

**16.** Which isolation level prevents dirty reads?
- A) READ UNCOMMITTED  B) READ COMMITTED
- C) REPEATABLE READ  D) SERIALIZABLE
<details><summary>Answer</summary>B) READ COMMITTED (and higher)</details>

**17.** What is denormalization?
- A) Removing redundancy  B) Adding redundancy for performance
- C) Creating indexes  D) Deleting data
<details><summary>Answer</summary>B) Adding redundancy for performance</details>

**18.** Which command is used to add a column to existing table?
- A) ADD COLUMN  B) ALTER TABLE  C) MODIFY  D) UPDATE
<details><summary>Answer</summary>B) ALTER TABLE ... ADD COLUMN</details>

**19.** What does the UNION operator do?
- A) Joins tables  B) Combines result sets removing duplicates
- C) Filters data  D) Groups data
<details><summary>Answer</summary>B) Combines result sets removing duplicates</details>

**20.** Difference between UNION and UNION ALL?
- A) UNION removes duplicates  B) UNION ALL keeps duplicates
- C) UNION ALL is faster  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**21.** What is an index in DBMS?
- A) Data structure for faster retrieval  B) Constraint
- C) View  D) Stored procedure
<details><summary>Answer</summary>A) Data structure for faster retrieval</details>

**22.** Which aggregate function returns average?
- A) AVG()  B) MEAN()  C) AVERAGE()  D) SUM()
<details><summary>Answer</summary>A) AVG()</details>

**23.** What is a stored procedure?
- A) Saved query  B) Precompiled SQL code
- C) Table  D) Index
<details><summary>Answer</summary>B) Precompiled SQL code</details>

**24.** Which constraint ensures uniqueness?
- A) PRIMARY KEY  B) UNIQUE  C) FOREIGN KEY  D) Both A and B
<details><summary>Answer</summary>D) Both A and B</details>

**25.** What is a trigger?
- A) Automatic action on event  B) Manual query
- C) Constraint  D) Index
<details><summary>Answer</summary>A) Automatic action on event</details>

**26.** Which is not a type of constraint?
- A) PRIMARY KEY  B) FOREIGN KEY  C) INDEX  D) CHECK
<details><summary>Answer</summary>C) INDEX (It's not a constraint)</details>

**27.** What does COMMIT do?
- A) Saves transaction  B) Rolls back  C) Deletes data  D) Creates table
<details><summary>Answer</summary>A) Saves transaction permanently</details>

**28.** What is referential integrity?
- A) Foreign key constraint  B) Primary key constraint
- C) Ensures valid references between tables  D) Both A and C
<details><summary>Answer</summary>D) Both A and C</details>

**29.** Which clause limits number of rows returned?
- A) LIMIT  B) TOP  C) ROWNUM  D) Depends on DBMS
<details><summary>Answer</summary>D) Depends on DBMS (LIMIT in MySQL, TOP in SQL Server)</details>

**30.** What is the purpose of DISTINCT keyword?
- A) Sort data  B) Remove duplicates  C) Group data  D) Filter data
<details><summary>Answer</summary>B) Remove duplicates from result set</details>

---

## 📚 Section 2: Object-Oriented Programming (OOP)

### **Key Concepts:**

#### **4 Pillars of OOP:**
1. **Encapsulation:** Bundling data and methods, hiding internal details
2. **Inheritance:** Child class inherits from parent
3. **Polymorphism:** Same interface, different implementations
4. **Abstraction:** Hiding complexity, showing only essentials

#### **Types:**
- **Static Polymorphism:** Compile-time (Method Overloading)
- **Dynamic Polymorphism:** Runtime (Method Overriding)
- **Single Inheritance:** One parent
- **Multiple Inheritance:** Multiple parents (not in Java, yes in C++)

---

### **OOP MCQs (30 Questions):**

**1.** Which is not a pillar of OOP?
- A) Encapsulation  B) Inheritance  C) Compilation  D) Polymorphism
<details><summary>Answer</summary>C) Compilation</details>

**2.** What is encapsulation?
- A) Hiding data  B) Bundling data and methods
- C) Access control  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**3.** Which keyword is used for inheritance in Java?
- A) inherits  B) extends  C) implements  D) import
<details><summary>Answer</summary>B) extends (for classes)</details>

**4.** What is method overloading?
- A) Same name, different parameters (compile-time)
- B) Same name, same parameters
- C) Runtime polymorphism  D) None
<details><summary>Answer</summary>A) Same name, different parameters (compile-time)</details>

**5.** What is method overriding?
- A) Compile-time polymorphism  B) Redefining parent method in child
- C) Same as overloading  D) None
<details><summary>Answer</summary>B) Redefining parent method in child (runtime)</details>

**6.** Can we override static methods in Java?
- A) Yes  B) No  C) Depends  D) Only in child class
<details><summary>Answer</summary>B) No (method hiding, not overriding)</details>

**7.** What is an abstract class?
- A) Cannot be instantiated  B) Can have abstract methods
- C) Can have concrete methods  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**8.** Difference between abstract class and interface?
- A) Interface has only abstract methods (Java 7)
- B) Class can implement multiple interfaces
- C) Abstract class can have constructors  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**9.** What is a constructor?
- A) Special method to initialize object
- B) Same name as class  C) No return type  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**10.** Can constructor be private?
- A) No  B) Yes (Singleton pattern)  C) Only in abstract class  D) None
<details><summary>Answer</summary>B) Yes (used in Singleton pattern)</details>

**11.** What is 'this' keyword?
- A) Refers to current object  B) Refers to parent
- C) Refers to class  D) None
<details><summary>Answer</summary>A) Refers to current object instance</details>

**12.** What is 'super' keyword?
- A) Refers to parent class  B) Calls parent constructor
- C) Accesses parent methods  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**13.** Can we overload main method in Java?
- A) Yes  B) No  C) Only in child class  D) None
<details><summary>Answer</summary>A) Yes (but JVM calls String[] version)</details>

**14.** What is the access level of private?
- A) Within class only  B) Within package
- C) Subclasses  D) Everywhere
<details><summary>Answer</summary>A) Within class only</details>

**15.** What is multiple inheritance problem in Java?
- A) Diamond problem  B) Not supported for classes
- C) Solved using interfaces  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**16.** What is polymorphism?
- A) One interface, multiple implementations
- B) Method overloading  C) Method overriding  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**17.** Can we declare interface methods as private?
- A) No (Java 7)  B) Yes (Java 9+)  C) Only static  D) None
<details><summary>Answer</summary>B) Yes (from Java 9 onwards)</details>

**18.** What is a final class?
- A) Cannot be inherited  B) All methods are final
- C) Cannot be instantiated  D) None
<details><summary>Answer</summary>A) Cannot be inherited</details>

**19.** What is a static method?
- A) Belongs to class, not instance  B) Can be called without object
- C) Cannot access instance variables  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**20.** What is aggregation?
- A) "Has-a" relationship  B) Weak association
- C) Objects can exist independently  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**21.** What is composition?
- A) Strong "has-a" relationship  B) Contained object cannot exist independently
- C) Stronger than aggregation  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**22.** Can interface have constructors?
- A) Yes  B) No  C) Only private  D) Only default
<details><summary>Answer</summary>B) No</details>

**23.** What is garbage collection?
- A) Automatic memory management  B) Removes unused objects
- C) Done by JVM  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**24.** Can we create object of abstract class?
- A) Yes  B) No  C) Only with new keyword  D) None
<details><summary>Answer</summary>B) No (directly, but can via child class)</details>

**25.** What is method signature?
- A) Method name + parameters  B) Return type
- C) Access modifier  D) All
<details><summary>Answer</summary>A) Method name + parameter types</details>

**26.** What is tight coupling?
- A) High dependency between classes  B) Low maintainability
- C) Hard to change  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**27.** What is loose coupling?
- A) Low dependency  B) High maintainability
- C) Uses interfaces  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**28.** What is the Singleton pattern?
- A) Only one instance of class  B) Private constructor
- C) Static method to get instance  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**29.** Can we override private methods?
- A) Yes  B) No (not visible to child)  C) Only in same package  D) None
<details><summary>Answer</summary>B) No (not inherited, so can't override)</details>

**30.** What is the default value of instance variables?
- A) 0 for numeric  B) false for boolean
- C) null for objects  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

---

## 📚 Section 3: Operating Systems (OS)

### **Key Concepts:**

#### **Process States:**
- New → Ready → Running → Waiting → Terminated

#### **Scheduling Algorithms:**
- **FCFS:** First Come First Serve
- **SJF:** Shortest Job First
- **Round Robin:** Time quantum based
- **Priority:** Based on priority

#### **Memory Management:**
- **Paging:** Fixed-size blocks
- **Segmentation:** Variable-size blocks
- **Virtual Memory:** Uses disk as RAM extension

---

### **OS MCQs (25 Questions):**

**1.** What is an operating system?
- A) Interface between user and hardware  B) Resource manager
- C) Program executor  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**2.** What is a process?
- A) Program in execution  B) Has process ID
- C) Has states  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**3.** Difference between process and thread?
- A) Thread is lightweight  B) Threads share memory
- C) Process has separate memory  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**4.** What is context switching?
- A) Switching between processes  B) Saves process state
- C) Overhead  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**5.** What is deadlock?
- A) Processes wait indefinitely  B) Four conditions
- C) Resource allocation issue  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**6.** Four conditions for deadlock?
- A) Mutual Exclusion, Hold and Wait, No Preemption, Circular Wait
- B) Only Circular Wait  C) Only Mutual Exclusion  D) None
<details><summary>Answer</summary>A) All four conditions must hold</details>

**7.** What is paging?
- A) Memory management technique  B) Divides memory into fixed-size pages
- C) Eliminates external fragmentation  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**8.** What is thrashing?
- A) Too much page swapping  B) Low CPU utilization
- C) High page fault rate  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**9.** What is a semaphore?
- A) Synchronization tool  B) Integer variable
- C) Uses wait() and signal()  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**10.** Difference between semaphore and mutex?
- A) Mutex is binary semaphore  B) Mutex for mutual exclusion
- C) Semaphore can be counting  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**11.** What is virtual memory?
- A) Uses disk as RAM  B) Allows larger programs
- C) Uses paging/segmentation  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**12.** What is a page fault?
- A) Requested page not in memory  B) Must fetch from disk
- C) Causes interrupt  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**13.** What is FCFS scheduling?
- A) First Come First Serve  B) Non-preemptive
- C) Can cause convoy effect  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**14.** What is Round Robin scheduling?
- A) Uses time quantum  B) Preemptive
- C) Fair scheduling  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**15.** What is priority scheduling?
- A) Based on priority  B) Can be preemptive or non-preemptive
- C) Can cause starvation  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**16.** What is critical section?
- A) Code accessing shared resource  B) Needs synchronization
- C) Only one process at a time  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**17.** What is external fragmentation?
- A) Free memory scattered  B) Total memory sufficient but not contiguous
- C) Solved by compaction  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**18.** What is internal fragmentation?
- A) Allocated memory larger than needed  B) Wasted memory within partition
- C) Occurs in paging  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**19.** What is spooling?
- A) Simultaneous Peripheral Operations OnLine
- B) Used in printing  C) Buffering  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**20.** What is a system call?
- A) Interface to OS services  B) Switches to kernel mode
- C) Examples: open(), read(), write()  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**21.** What is inter-process communication (IPC)?
- A) Communication between processes  B) Shared memory, message passing
- C) Pipes, sockets  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**22.** What is the difference between kernel mode and user mode?
- A) Kernel mode: full hardware access  B) User mode: restricted access
- C) Switching has overhead  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**23.** What is a zombie process?
- A) Completed but entry in process table  B) Parent didn't read status
- C) Takes up process ID  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**24.** What is an orphan process?
- A) Parent terminated before child  B) Adopted by init process
- C) Still runs normally  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**25.** What is aging in OS?
- A) Prevents starvation  B) Gradually increases priority
- C) Used in priority scheduling  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

---

## 📚 Section 4: Computer Networks

### **Key Concepts:**

#### **OSI Model (7 Layers):**
1. Physical → 2. Data Link → 3. Network → 4. Transport → 5. Session → 6. Presentation → 7. Application

#### **TCP/IP Model (4 Layers):**
1. Network Access → 2. Internet → 3. Transport → 4. Application

#### **Protocols:**
- **HTTP:** Port 80 (Web)
- **HTTPS:** Port 443 (Secure Web)
- **FTP:** Port 21 (File Transfer)
- **SSH:** Port 22 (Secure Shell)
- **SMTP:** Port 25 (Email)
- **DNS:** Port 53 (Domain Name)

---

### **Networks MCQs (25 Questions):**

**1.** How many layers in OSI model?
- A) 5  B) 7  C) 4  D) 6
<details><summary>Answer</summary>B) 7</details>

**2.** Which layer is responsible for routing?
- A) Data Link  B) Network  C) Transport  D) Application
<details><summary>Answer</summary>B) Network Layer</details>

**3.** What is the protocol used at Network layer?
- A) TCP  B) IP  C) HTTP  D) FTP
<details><summary>Answer</summary>B) IP (Internet Protocol)</details>

**4.** What is the difference between TCP and UDP?
- A) TCP is connection-oriented  B) UDP is connectionless
- C) TCP ensures delivery  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**5.** What is the default port for HTTP?
- A) 21  B) 80  C) 443  D) 22
<details><summary>Answer</summary>B) 80</details>

**6.** What is the default port for HTTPS?
- A) 80  B) 443  C) 8080  D) 22
<details><summary>Answer</summary>B) 443</details>

**7.** What does DNS do?
- A) Translates domain name to IP  B) Domain Name System
- C) Uses port 53  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**8.** What is an IP address?
- A) Unique identifier for devices  B) Can be IPv4 or IPv6
- C) Logical address  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**9.** What is a MAC address?
- A) Physical address  B) Unique to network card
- C) 48-bit  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**10.** What is a subnet mask?
- A) Divides IP into network and host  B) Used in routing
- C) Example: 255.255.255.0  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**11.** What is HTTP?
- A) HyperText Transfer Protocol  B) Application layer protocol
- C) Stateless  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**12.** What is HTTPS?
- A) Secure HTTP  B) Uses SSL/TLS
- C) Encrypts data  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**13.** What is FTP?
- A) File Transfer Protocol  B) Port 21
- C) Used for file transfer  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**14.** What is a router?
- A) Connects different networks  B) Works at Network layer
- C) Routes packets  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**15.** What is a switch?
- A) Connects devices in LAN  B) Works at Data Link layer
- C) Uses MAC addresses  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**16.** What is a hub?
- A) Connects devices  B) Works at Physical layer
- C) Broadcasts to all  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**17.** Difference between hub and switch?
- A) Switch is intelligent  B) Switch uses MAC table
- C) Hub broadcasts  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**18.** What is a gateway?
- A) Connects different protocols  B) All layers
- C) Protocol converter  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**19.** What is ARP?
- A) Address Resolution Protocol  B) Maps IP to MAC
- C) Network/Data Link layer  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**20.** What is DHCP?
- A) Dynamic Host Configuration Protocol
- B) Assigns IP automatically  C) Port 67/68  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**21.** What is NAT?
- A) Network Address Translation  B) Private to public IP
- C) Conserves IP addresses  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**22.** What is a firewall?
- A) Security system  B) Filters traffic
- C) Blocks unauthorized access  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**23.** What is bandwidth?
- A) Maximum data transfer rate  B) Measured in bps
- C) Network capacity  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**24.** What is latency?
- A) Time delay  B) Measured in ms
- C) Affects performance  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

**25.** What is the three-way handshake in TCP?
- A) SYN → SYN-ACK → ACK  B) Establishes connection
- C) Ensures reliability  D) All of the above
<details><summary>Answer</summary>D) All of the above</details>

---

## ✅ Practice Schedule

**Daily Target:** 15-20 MCQs (30 minutes)

### Week Distribution:
- **Days 3-4:** DBMS (15 Qs each day)
- **Days 5-6:** OOP (15 Qs each day)
- **Week 2:** OS (15 Qs) + Networks (15 Qs)

---

## 🎯 Quick Revision Points

### **DBMS:**
- Normalization forms
- ACID properties
- JOIN types
- Aggregate functions

### **OOP:**
- 4 Pillars
- Overloading vs Overriding
- Abstract class vs Interface
- Access modifiers

### **OS:**
- Process states
- Deadlock conditions
- Scheduling algorithms
- Paging vs Segmentation

### **Networks:**
- OSI layers
- TCP vs UDP
- Common ports
- IP addressing

---

**Master these concepts for guaranteed Technical MCQ success!**
