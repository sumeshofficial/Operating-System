### Persistence in Operating Systems

### What Is Persistence?

Persistence means keeping data safe and permanent, even after the system shuts down or restarts.
In simple words, persistence ensures that data doesn’t disappear when power is lost or the computer crashes.

### Why Persistence Is Important

When we perform operations like create, read, update, or delete,
there’s always a chance that the system may crash midway — for example, during a power failure or software error.

If the data was only stored in volatile memory (like RAM),
then all that data would be lost immediately after the crash.
That’s because RAM clears its contents when the power goes off.

### How the OS Solves This Problem

To solve this, the Operating System uses non-volatile storage devices like SSDs or Hard Drives (HDDs).
These devices retain data permanently, even when the system is turned off.

The OS handles these storage devices through a **File Management System**.
This system keeps track of:

- Where each file is stored

- How to read and update data

- How to create and delete files

- How to recover data safely after a crash

### File Management in the OS

The **File Manager** is a core component of the Operating System that:

- Organizes data into files and directories

- Keeps track of file locations on disk

- Controls permissions (who can access or modify files)

- Handles I/O operations safely and efficiently

Unlike **virtual memory**, file management deals with actual physical data stored on disk.
It ensures your data remains persistent and protected from system failures.