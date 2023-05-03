Download Link: https://assignmentchef.com/product/solved-cs314-lab-7
<br>
5/5 - (1 vote)

Implement immediate files in the Minix File System, for files of size up to 32 bytes. Implement only for the file system mounted at /home.

Think about what functionalities need to be changed to implement immediate files. Some broad points:

<ul>

 <li>●  File creation: you can start by creating the file as an immediate one. When a file grows beyond 32B, then you can make it a regular file.</li>

 <li>●  File read: if it is an immediate file, you can respond with the inode structure contents. If not, you can follow the default behavior of looking up zones.</li>

 <li>●  File write: similar to read. You must take care to ensure that if you want to write to the inode structure, then the new file size is still within 32B. When a regular file shrinks to less than 32 bytes, there is no need to come back to immediate mode.</li>

 <li>●  File delete: deleting immediate files does not require any handling of zones.Helpful files:● www.minix3.org/theses/gerofi-minix-vfs.pdf</li>

</ul>