# Operating Systems Review Questions and Problems.


## Chapter 10 File Systems

1. In an EXT-filesystem, how many inodes does a file have?
	
	1.1 What the hell are inodes?
	https://www.howtogeek.com/465350/everything-you-ever-wanted-to-know-about-inodes-on-linux/
	
	The Linux file system relies on inodes.

	In the Linux ext4 file system, the inode and directory structures work together to provide an underpinning framework that stores all the metadata for every file and directory. They make the metadata available to anyone who requires it, whether that’s the kernel, user applications, or Linux utilities, such as ls, stat, and df.

	Answer: I guess it's got only 1?


2. Hva menes med ekstern og intern fragmentering i forbindelse med en fil?

	2.A What the hell is fragmentation to begin with?

	https://afteracademy.com/blog/what-is-fragmentation-and-what-are-its-types

	In contiguous memory allocation whenever the processes come into RAM, space is allocated to them. These spaces in RAM are divided either on the basis of fixed partitioning(the size of partitions are fixed before the process gets loaded into RAM) or dynamic partitioning (the size of the partition is decided at the run time according to the size of the process). As the process gets loaded and removed from the memory these spaces get broken into small pieces of memory that it can’t be allocated to the coming processes. This problem is called fragmentation.

	2.1 What is external fragmentation?

	![External Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20200729172413/2581.png)


	2.2 What is internal fragmentation?

	![Internal Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20190924115421/Untitled-Diagram-146.png)

	Internal fragmentation happens when the memory is split into mounted size blocks. When a method or a program runs, it uses alloted blocks. Internal fragmentation is then the difference between the required space and the memory allocated. 



