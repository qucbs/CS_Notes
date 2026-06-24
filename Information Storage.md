Rather than accessing individual bits of memory, a computer uses blocks of 8 bits, or a byte as the smallest addressable unit of memory.
A machine level program views memory as a <span style="color:rgb(231, 24, 176)">very large array to bytes</span>, referred to as <span style="color:rgb(231, 24, 176)">virtual memory</span>.
Every byte of memory is identified by a unique number, known as its address, and<span style="color:rgb(231, 24, 176)"> the set of all possible addresses is known as the virtual address space</span>.


**Data Sizes**
Every computer has a word size, indicating the nominal size of pointer data. Since a virtual address is encoded by such a word, the most important system parameter determined by the word size is the maximum size of the virtual address space. That is, for a machine with a w-bit word size, the virtual addresses can range from 0 to 2^w − 1, giving the program access to at most 2^w bytes. 

(where a 'word' is the natural amount of data the processor can work with)

---

*Typical sizes (in bytes) of basic C data types*

![[image 4.png]]


**Ordering the bytes that together represent an object**
![[image-1 1.png]]

![[image-2 1.png]]







