## What is CryoPID? ##

**CryoPID** can move your running Linux programs from one computer to another.

The CryoPID process freezer is a simple user-space Linux tool that scans the memory of a running Linux process, compresses a **snapshot**, and adds some loader code at the beginning to create for you a self-archiving, self-extracting process migration tool.

## Why would I want to use it? ##

If you have a long-running process on a Linux machine with state that is inconvenient to lose, you might want to consider a snapshotting tool like CryoPID.

For example ...

  * A coder familiar with a bug could open a source editor, launch the buggy program in a debugger, step right up to the problem area, and then **freeze** the entire resulting environment. Another coder could then use the frozen state to restart an identical set of tools right where the first coder left off. The second coder could begin looking at the problem right away, without needing to set up a complicated development environment and hope that it is a close enough match.

  * A number cruncher with a program to calculate pi to millions of digits could have been running it at home since last year. If the weather forecast predicts thunderstorms, the cruncher could use CryoPID to snapshot the state of the running program, potentially saving months of work from being lost to a power outage.


## What is the status of the code? ##

The current release seems to work fine now on Debian Lenny and CentOS 5.4.

Newer Linux kernels have changed the way that processes are organized. Unfortunately, earlier developers of CryoPID have not had the non-trivial amounts of time for tracking the internals of each new kernel version. Newer (and older) releases no longer work correctly.

We are actively trying to close this gap.