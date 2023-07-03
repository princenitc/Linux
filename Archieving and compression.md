# Archiving and Compression

__Archiving__ : Combines multiple files into one, which eliminates the overhead in individual files and makes the files easier to transmit.

__Compression__ : Makes the files smaller by removing redundant information.
    - _Lossless_ : No information is removed from the file. Compressing a file and decompressing it leaves something identical to the original.
    - _Lossy_ :  Information might be removed from the file. It is compressed in such a way that uncompressing a file will result in a file that is slightly different from the original.

- _gzip <filename>_  : Compresses the file in .gz(Gunzip)
- _gunzip/gzip <compressedfilename> : Decompresses a file.
- __Tape Archive(tar)__ : Tar has three modes that are helpful to be familiar : 
    - _Create_ : Make a new archive out of a series of files.
    - _Extract_ : Pull one or more file out of archive
    - _List_ : Show the contents of archive without extracting.
    