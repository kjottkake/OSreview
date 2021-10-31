# Operating Systems Review Questions and Problems.


## Chapter 10 File Systems

1. In an EXT-filesystem, how many inodes does a file have?
	
	1.1 What the hell are inodes?
	https://www.howtogeek.com/465350/everything-you-ever-wanted-to-know-about-inodes-on-linux/
	
	The Linux file system relies on inodes.

	In the Linux ext4 file system, the inode and directory structures work together to provide an underpinning framework that stores all the metadata for every file and directory. They make the metadata available to anyone who requires it, whether that’s the kernel, user applications, or Linux utilities, such as ls, stat, and df.

	Answer: I guess it's got only 1?


2. Hva menes med ekstern og intern fragmentering i forbindelse med en fil?

	2.1 What is external fragmentation?

	![External Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20200729172413/2581.png)


	2.2 What is internal fragmentation?

	![Internal Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20190924115421/Untitled-Diagram-146.png)



