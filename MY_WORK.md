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
| **Full Name** | Ghadi Bader Alshedi |
| **Student ID** | 446051748 |
| **University Email** | 446051748@std.psau.edu.sa |
| **GitHub Username** | Ghadi-bader48 |
| **Repository Link** | https://github.com/Ghadi-bader48/OS-Assignment3-Ghadi-Alshedi |
 
---

## 🎥 Video Link

**Video Link**: Not uploaded yet.

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

### Entry 1 - [November 5, 2026, 10:00 PM]
**What I did**: Prepared the GitHub project and entered my student ID.

**Details**: I forked the instructor's repository and changed `studentID` to `446051748` in `SchedulerSimulationSync.java`. I also learned the steps for making a commit and pushing it to GitHub.

**Challenges**: At first, I was not sure how to stage a changed file and save it as a commit.

**Solution**: I reviewed the Git steps and checked the repository after pushing the change.

**Time spent**: 30 minutes

---

### Entry 2 - [November 5, 2026, 11:30 PM]
**What I did**: Worked on Feature 1, which protects the ready queue.

**Details**: I added `queueLock` to `ReadyQueue` and used it in `add()`, `poll()`, `processOf()`, and `snapshot()`. The `finally` block releases the lock after each operation.

**Challenges**: I had difficulty placing the braces around the `try` and `finally` blocks.

**Solution**: I checked the methods carefully and corrected the braces so that the lock is always released.

**Time spent**: 45 minutes

---

### Entry 3 - [November 11, 2026, 3:45 PM]
**What I did**: Worked on the shared counters and CPU waiting.

**Details**: I used one `statsLock` for the three statistics and their getters. I also added `availableProcesses`, a counting `Semaphore`, so a CPU waits for a permit before removing a process from the queue.

**Challenges**: I needed to protect the counters and stop CPUs from repeatedly checking an empty queue.

**Solution**: I used `lock()` with `try/finally` for the statistics and `acquire()` with `release()` for the queue permits.

**Time spent**: 15 minutes

---

### Entry 4 - [November 11, 2026, 4:00 PM]
**What I did**: Tested the scheduler after the synchronization changes.

**Details**: I checked the four verification values and made sure the program could finish without a watchdog warning. 

**Challenges**: I wanted to make sure no process was lost and that CPU waiting did not continue after execution finished.

**Solution**: I compared the expected results with the observed results and checked the shutdown logic in `CpuWorker.run()`.

**Time spent**: 25 minutes

---

### Entry 5 - [November 11, 2026, 5:00 PM]
**What I did**: Started writing the assignment documentation.

**Details**: I reviewed the separate feature commits, entered my student information, and organized the development log under the instructor's headings.

**Challenges**: Some questions needed specific examples from the code rather than a general explanation.

**Solution**: I read the related Java methods and connected each answer to the code it describes.

**Time spent**: 1 hour

---

### Entry 6 - [November 11, 2026, 10:00 PM]
**What I did**: Checked the three synchronization features together.

**Details**: I reviewed the queue lock, statistics lock, and semaphore in `ReadyQueue`, `SharedStats`, and `CpuWorker`. I also checked the `null` result after `poll()` and the permit release used at shutdown.

**Challenges**: An earlier run had a `NullPointerException` because more than one CPU could try to remove a queue item at the same time.

**Solution**: I checked that shared queue operations use `queueLock` and that a CPU checks for `null` before using the selected process.

**Time spent**: 1 hour

---

### Entry 7 - [November 13, 2026, 6:40 PM]
**What I did**: Completed the Reflection and Technical Answers in MY_WORK.md.

**Details**: 
- Answered the four Reflection questions in Part B.
- Completed the four Technical questions in Part C.
- Used the results from the original and final runs to explain the race condition and synchronization.
- Explained the locks, semaphore, busy waiting, and deadlock using examples from the code.

**Challenges**: Some technical questions needed more explanation, especially the race condition, lock granularity, and deadlock prevention.

**Solution**:I reviewed the relevant Java methods and compared the execution results to make sure my answers were clear and correct.

**Time spent**: 60 minutes

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: 5 hours 

**Most challenging part**: Making sure the CPU workers stop correctly after the last process has finished.

**Most interesting learning**: A mutex protects shared values, while a semaphore allows a thread to wait until there is work.

**What I would do differently next time**: I would update the work file after each feature.

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

I learned that synchronization is important when several threads use the same data. The original scheduler had a race condition because two CPUs could access the ready queue at the same time. A `ReentrantLock` makes a critical section run with mutual exclusion. I also used `try/finally` so the lock is released even when a method returns. The three shared statistics need protection during both updates and reads. The `Semaphore` has a different purpose because it allows a CPU to wait until there is a ready process.

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

The hardest part for me was understanding the CPU waiting and shutdown behavior. A CPU should not keep checking the ready queue when it is empty. Using `acquire()` solves that problem by blocking the CPU until a permit is available. However, a CPU may still be blocked when the last process finishes. I had to understand why the final `release(totalCPUs)` is necessary. That release allows blocked CPUs to wake up and finish their loops.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

I worked through the synchronization features one part at a time. First, I checked the shared queue and added `queueLock` to the methods that access it. Next, I added `statsLock` to stop the counters from losing updates. I then connected the `Semaphore` to adding and taking processes from the queue. I reviewed the code to make sure locks were released in `finally` blocks. I ran my final code five times in a row, and every run finished all 11 processes with zero busy-waiting polls.

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

Synchronization is useful in systems where many users share the same information. For example, an online ticket system may have two people trying to book the last available seat. Without a lock, both requests might read the same seat as available. A mutex can protect the booking step so the seat is assigned only once. Another example is a print queue used by several computers. A semaphore can let a printer worker wait until there is a print job instead of checking the queue again and again.

### Optional: What would you like to learn more about?

I would like to understand fair locks and how they affect waiting threads.

### Optional: How confident do you feel about synchronization concepts now?

Intermediate. I understand the basic use of `ReentrantLock` and `Semaphore`, but I need more practice with deadlock cases.

### Optional: Feedback on the assignment

The assignment helped me understand race conditions because I could compare the broken and working program.

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

In the original starter run, CPU-1 and CPU-2 threw a `NullPointerException`, and the simulation recorded 0 context switches instead of 24, 0 completed processes instead of 11, and 0 ms instead of 83,598 ms. This happened because the CPUs could enter the unprotected queue code at the same time, so a thread could change the queue while another one was removing an item. A lost update can also happen in `contextSwitchCount`: CPU-1 reads 5, CPU-2 reads 5 during `RaceWindow.pause()`, and both write 6 instead of reaching 7. The same timing problem can happen on a real CPU without the added pause, and it is difficult to find because the thread order can change between runs.

Verification block of the **original starter**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 24       observed 0        ? MISMATCH
  Completed processes                    expected 11       observed 0        ? MISMATCH
  Total service time (ms)                expected 83598    observed 0        ? MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 0        ?
  ? At least one check failed (see the ? lines above): a race condition or busy waiting is still present.
```

Verification block of **my final version**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 24       observed 24       ?
  Completed processes                    expected 11       observed 11       ?
  Total service time (ms)                expected 83598    observed 83598    ?
  Busy-waiting polls (must be 0)         expected 0        observed 0        ?
  ? All shared values are consistent.
```

**Explanation of the timeline:**
CPU-1 and CPU-2 both read the same old counter value before either writes it back. After the pause, both save the same new value, so one increment is lost. The example above shows a possible race; the captured starter run failed earlier with the queue exception.

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

I protected `ReadyQueue.add()`, `poll()`, `processOf()`, and `snapshot()` with `queueLock` because those methods share the same `list` and `map`. I chose one `statsLock` for the three statistics and their getter methods because this is easy to manage, although two updates to different counters may need to wait for each other. The ready queue has a different lock so queue operations and statistics updates do not all wait on one mutex. The `try/finally` blocks always release the locks, which supports mutual exclusion and lets other threads make progress, but the default non-fair `ReentrantLock` cannot guarantee bounded waiting.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| `ReadyQueue.add()` and `poll()` (`list`, `map`) | `queueLock` | Prevent two CPUs from changing the queue at the same time. |
| `ReadyQueue.processOf()` and `snapshot()` | `queueLock` | Protect reads while another CPU may update the list or map. |
| `incrementContextSwitch()` and `getContextSwitchCount()` | `statsLock` | Avoid lost increments and incorrect reads. |
| `incrementCompletedProcess()` and `getCompletedProcessCount()` | `statsLock` | Keep the finished-process count correct. |
| `addServiceTime()` and `getTotalServiceTime()` | `statsLock` | Protect the total service time from overlapping updates. |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

The original starter uses busy waiting when a CPU finds an empty queue, which means it checks again after sleeping and wastes CPU activity; my captured starter run showed 0 polls only because both CPUs crashed before reaching that stage. The `availableProcesses` semaphore represents the number of ready-process permits, starts at 0, and reaches 11 just after the first 11 `add()` calls because the CPU workers have not started taking items yet. Each `add()` calls `release()` to provide one permit, and each worker calls `acquire()` to wait for one before polling the queue. After the last process finishes, the worker releases `totalCPUs` permits so blocked CPU threads can wake and stop; without this release, a waiting worker could remain blocked forever.

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
This scheduler is an example of the producer-consumer problem. The main thread produces the starting queue entries, and the CPU workers consume them, but a CPU also becomes a producer when it places an unfinished process back in the queue.

**Semaphores for a bounded queue (name and initial value)**:
A queue with capacity `K` would use `empty = K`, `full = 0`, and `mutex = 1`.

**Deadlock scenario and prevention**:
If a producer holds `mutex` while waiting for `empty` when the queue is full, a consumer cannot take a process because it also needs `mutex`. Waiting for `empty` before locking `mutex` avoids holding one resource while waiting for another and breaks the hold-and-wait condition.

## Summary

**Key concepts I understood through these questions:**
1. Protecting a shared queue with a mutex.
2. Keeping statistics correct when multiple threads run.
3. Using a semaphore to avoid busy waiting.

**Concepts I need to study more:**
1. Fair scheduling and bounded waiting.
2. More examples of deadlock prevention.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [x] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [x] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [x] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [x] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [x] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [x] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [x] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [x] **The four verification lines are ✔ in 5 consecutive runs**
- [x] Every lock is released in a `finally` block
- [x] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [x] Each feature has clear comments

**Commits**
- [x] **At least 4 meaningful commits, ideally 7 or more**
- [x] **One commit per feature**
- [x] Commits are spread over **different dates** (not all in the last hour)
- [x] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [x] Full name and student ID filled in at the top
- [x] Development log has **5+ entries** on different dates
- [x] Reflection: 4 questions, 5-7 sentences each
- [x] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [x] No `[...]` placeholders left
- [x] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [x] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
