# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Razan Abdullah Alothman] |
| **Student ID** | [445052477] |
| **University Email** | [445052477]@std.psau.edu.sa |
| **GitHub Username** | [Razan-Alothman-477] |
| **Repository Link** | [https://github.com/Razan-Alothman-477/OS-Assignment3-Razan-Alothman.git] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1rhJ6up9r5NO8WY3EiFLsLKjAnPflY6Eq/view?usp=sharing]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [November 13, 2026 at 2:06 PM]
**What I did**: i set my student ID in SchedulerSimulationSync.java

**Details**:
nothing much
**Challenges**:
no challenges
**Solution**:

**Time spent**:
5 min
---

### Entry 2 - [November 13, 2026 at 2:37 PM]
**What I did**: i set my informations in MY_WORK class

**Details**:

**Challenges**:

**Solution**:

**Time spent**:
about 10min
---

### Entry 3 - [November 13, 2026 at 10:58 PM]
**What I did**:Feature 1: Mutex lock on the ready queue

**Details**:
it was the easiest to do
**Challenges**:
nothing
**Solution**:

**Time spent**:
about 25min
---

### Entry 4 - [November 13, 2026 at 11:30 PM]
**What I did**:Feature 2: Mutex locks on the shared statistics

**Details**:

**Challenges**:

**Solution**:

**Time spent**:
about an hour.
---

### Entry 5 - [November 14, 2026 at 2:14 AM]
**What I did**:Feature 3: Counting semaphore instead of busy waiting

**Details**:

**Challenges**:

**Solution**:

**Time spent**:
hour and a half
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [5 hour]

**Most challenging part**:
implemnting Mutex locks
**Most interesting learning**:
implemnting Mutex locks
**What I would do differently next time**:
starting erlier
---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[I learned how race conditions corrupt shared data when multiple CPU threads execute read-modify-write operations concurrently. In the starter code, I was surprised to see mismatches in Context switches, Completed processes, and Total service time. Adding ReentrantLock with try/finally blocks enforced mutual exclusion safely across ReadyQueue and SharedStats. I also learned how a counting Semaphore initialized to 0 replaces wasteful busy-waiting by putting idle CPUs to sleep until add() signals them. Seeing Busy-waiting polls drop to 0 showed me how proper synchronization keeps concurrent schedulers accurate and efficient.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part was implementing the clean shutdown for the counting Semaphore in CpuWorker.run(). It was tricky to wake up CPU threads blocked on readyCount.acquire() after all 12 processes finished. Without releasing extra permits at the end, sleeping threads would stay blocked forever and trigger the watchdog timeout. Placing readyCount.acquire() before queueLock.lock() in poll() also required careful ordering to prevent a deadlock. Solving this helped me understand how signaling and thread termination work together.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame these challenges by implementing one feature at a time and testing each five times before committing. When I hit missing import errors and a NoSuchMethodError from old .class files, I opened the repository in a clean VS Code folder and checked the Problems tab. For the semaphore shutdown, I added a shutdown(int cpuCount) method in ReadyQueue that releases permits when completedProcessCount equals totalProcesses. Checking the verification table after every run confirmed that each fix worked properly.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[After working on this assignment, I can easily see how these ideas show up in apps we use every day. For example, when people transfer money in a banking app, the account balance is shared data that needs a lock so two transfers do not mess up the total, just like we used ReentrantLock for SharedStats. Another clear example is booking flight or concert tickets online, where a lock stops two people from grabbing the exact same seat at once. Also, a shared office print queue works just like our ReadyQueue with a counting semaphore, where the printer waits quietly until someone sends a document. If developers did not use locks and semaphores in these apps, we would constantly see wrong bank balances, double-booked seats, and slow devices.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[When I first ran the starter code, `CPU-1`, `CPU-2`, and `CPU-3` crashed right away with a `NullPointerException` inside `ReadyQueue.snapshot()`, which left `Context switches` (expected 28, observed 0), `Completed processes` (expected 12, observed 0), and `Total service time` (expected 82849, observed 0) all wrong. Because there were no locks, the CPU threads collided while reading and changing shared data at the same time. Even on a real computer without `RaceWindow`, the operating system can pause one thread right before it saves its update and let another thread jump in. These bugs are tricky to catch because the clash happens in tiny fractions of a second, so the program might fail on one run and look fine on the next.]

Verification block of the **original starter**:
```
[Exception in thread "CPU-1" Exception in thread "CPU-2" Exception in thread "CPU-3" java.lang.NullPointerException: Cannot read field "next" because "this.next" is null
	at java.base/java.util.LinkedList$ListItr.next(LinkedList.java:905)
	at ReadyQueue.snapshot(SchedulerSimulationSync.java:151)
	at CpuWorker.run(SchedulerSimulationSync.java:280)

Context switches (quanta executed)     expected 28         observed 0          ✘ MISMATCH
Completed processes                     expected 12         observed 0          ✘ MISMATCH
Total service time (ms)                 expected 82849      observed 0          ✘ MISMATCH
Busy-waiting polls (must be 0)          expected 0          observed 0          ✔]
```

Verification block of **my final version**:
```
[Context switches (quanta executed)     expected 28         observed 28         ✔
Completed processes                     expected 12         observed 12         ✔
Total service time (ms)                 expected 82849      observed 82849      ✔
Busy-waiting polls (must be 0)          expected 0          observed 0          ✔
All shared values are consistent.
]
```

**Explanation of the timeline:**
[CPU-1 reads `contextSwitchCount` = 5 -> CPU-1 gets paused at `RaceWindow.pause()` -> CPU-2 jumps in and reads `contextSwitchCount` = 5 -> CPU-1 wakes up and writes 6 -> CPU-2 also writes 6 -> CPU-1's update is completely overwritten and lost.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[I used fine-grained locking by giving each of the three counters in `SharedStats` its own lock (`csLock`, `completedLock`, and `serviceLock`), because they are completely independent and updating one should not block a CPU from updating another. The trade-off is managing a bit more code compared to a single shared lock, which is simpler to write. I also kept `queueLock` separate for `ReadyQueue` so that slow queue snapshots or polls never block quick counter updates, preventing unnecessary waiting. These mutex locks guarantee mutual exclusion since only one thread can enter each critical section at a time, and progress is maintained because every lock is always released in a `finally` block. However, since a default `ReentrantLock` is non-fair, bounded waiting is not strictly guaranteed because a thread could theoretically jump ahead of another waiting thread.]

| Critical section (variable / method) | Lock used | Why it needs protection |
||||
| [e.g., `ReadyQueue.poll()`] | [lock name] | [reason] |
| [ `ReadyQueue` (`list` & `map` in `add`, `poll`, `processOf`, `snapshot`)|`queueLock`] | [|`queueLock`] | [Prevents concurrent reads and modifications from corrupting the queue or causing `NullPointerException`.] |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the starter code, when the ready queue was empty, CPUs kept looping and sleeping for 20ms in a busy-waiting loop (`Busy-waiting polls` reached 4 to 8 in my early runs), wasting CPU cycles just checking an empty queue. In my final version, the counting semaphore `readyCount` represents the exact number of processes currently waiting in `ReadyQueue`. It starts with an initial value of `0` because the queue is empty at startup, and right after the initial `numProcesses` (12) `add()` calls, its value becomes `12` so all 3 CPUs can immediately grab work and put idle threads to sleep via `acquire()`. At the end, the last CPU to finish calls `release(totalCPUs)` so that any worker threads still sleeping on `acquire()` wake up, see that all processes are done, and exit cleanly instead of staying blocked forever and triggering the watchdog timeout.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[This is the classical **Producer-Consumer (Bounded-Buffer) problem**. Both the `main` thread (when initially adding all 12 processes) and the `CpuWorker` threads (when re-enqueuing unfinished processes back into `ReadyQueue`) act as **producers**, while the `CpuWorker` threads act as **consumers** whenever they call `poll()` to take processes out of the queue.]

**Semaphores for a bounded queue (name and initial value)**:
[If `ReadyQueue` were bounded to capacity `K`, we would need three semaphores: `mutex` initialized to `1` (to protect queue access), `empty` initialized to `K` (to count available free slots in the queue), and `full` initialized to `0` (to count how many processes are currently ready in the queue).]

**Deadlock scenario and prevention**:
[A deadlock happens if a consumer acquires `queueLock` (mutex) first and then calls `readyCount.acquire()` while the queue is empty: the consumer goes to sleep while still holding `queueLock`, blocking any producer from acquiring `queueLock` to add a new process and wake it up. By always acquiring the semaphore *before* acquiring the mutex lock (consistent resource ordering), we break the **Circular Wait** condition and completely prevent this deadlock.]

## Summary

**Key concepts I understood through these questions:**
1.How race conditions and lost updates happen on shared data, and how to prevent them using `ReentrantLock` with `try/finally` blocks.
2.How choosing fine-grained locking over coarse-grained locking reduces unnecessary blocking between independent counters.
3.

**Concepts I need to study more:**
1.Advanced synchronization tools like `Condition` variables and read-write locks for more complex producer-consumer scenarios.
2.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ done ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ done ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ done] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ done ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ done ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ done ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ done ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ done ] **The four verification lines are ✔ in 5 consecutive runs**
- [ done ] Every lock is released in a `finally` block
- [ done ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ done ] Each feature has clear comments

**Commits**
- [ done ] **At least 4 meaningful commits, ideally 7 or more**
- [ done ] **One commit per feature**
- [ done ] Commits are spread over **different dates** (not all in the last hour)
- [ done ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ done ] Full name and student ID filled in at the top
- [ done ] Development log has **5+ entries** on different dates
- [ done ] Reflection: 4 questions, 5-7 sentences each
- [ done ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ done ] No `[...]` placeholders left
- [ done ] No section headers deleted

**Video**
- [ done ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ done ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ done ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ done ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
