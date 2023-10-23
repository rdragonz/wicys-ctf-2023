# Cat Photos
A .img file of a flash drive that was dropped by a secret agent has been recovered and imaged.
Find a way to locate and extract the hidden flag.

## Forensics
Difficulty: Easy

## Solution
- Extract the presented .img file. From here there are two paths that can possibly be followed as the "Intended" solution.
- The first (but more complicated, as many may be unfamiliar with the software) path is to load the .img file into a digital forensics program such as [Autopsy](https://www.autopsy.com/), create a new case, add the .img file as a data source, and then view the "Deleted files" section under the data source to locate the Word document.
- The second, easier, method is to mount the disk image using a mounting program such as [OSFMount](https://www.osforensics.com/tools/mount-disk-images.html), and then use a deleted file scanning program such as [PhotoRec](https://www.cgsecurity.org/wiki/PhotoRec) to scan the image for deleted files.
- Either method will yield a Word document with a bonus cat picture and the flag WCS{D3L3T3M3}
- It's important to note that a recovery program must employ "File Carving".

A third, unintended but fully valid, solution is to simply print out the contents of the .img file and search for the string "WCS{" using grep. This was discovered by one creative individual who was not participating in the CTF but was given access to my challenges to test everything out! 

## Hint
What happens to deleted data?

## Explanation
For decades, digital forensics specialists have been using software to index and search through media recovered from crime scenes. This sometimes includes searching for files that were deleted. Since computers are lazy, data that is "deleted" by a user is not actually deleted. Instead, the space that the data once occupied is marked as available for re-use. Until it is re-used, the "deleted" data still remains, just without the associated filename/path/entry on the filesystem. It's possible to use software to scan a drive for these deleted files through a process known as "File Carving", which identifies known headers and data signatures to recover files.