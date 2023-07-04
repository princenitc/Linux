# Archiving and Compression

- __Archiving__ : Combines multiple files into one, which eliminates the overhead in individual files and makes the files easier to transmit.

- __Compression__ : Makes the files smaller by removing redundant information.
    - _Lossless_ : No information is removed from the file. Compressing a file and decompressing it leaves something identical to the original.
    - _Lossy_ :  Information might be removed from the file. It is compressed in such a way that uncompressing a file will result in a file that is slightly different from the original.

- _gzip filename_  : Compresses the file in .gz(Gunzip)
- _gunzip/gzip compressedfilename : Decompresses a file.
- __Tape Archive(tar)__ : Tar has three modes that are helpful to be familiar : 
    - _Create_ : Make a new archive out of a series of files.
    - _Extract_ : Pull one or more file out of archive
    - _List_ : Show the contents of archive without extracting.

    - __Create Mode__ : _tar -c [-f ARCHIVE] [OPTIONS] [FILE]_ : this command will generate the tar compressed file.
        - where -c -> Create an archive
        - -f -> Use archive file where, ARCHIVE is the name of the file which will be generated finally.
        - Example - tar -cf alpha_files.tar alpha* -----> creates alpha_files.tar from all input files.
        - -z -> option could be used along to create a zipped file of the corresponging tar file.
        - -j -> opation could be used to compress with bzip2 type compression.

    - __List Mode__ : tar -t [-f ARCHIVE] [OPTIONS] : Given a tar file compressed or not we can view the contents under it using -t option.
        - -t -> List the files in the archive
        - -j -> Decompresses with the bzip2 command
        - -f ARCHIVE -> Operates on the given archive.
        - example : tar -tjf folders.tbz
    - __Extract Mode__ : tar -x [-f ARCHIVE] [OPTIONS] : Can be used to extract a tar file.
        - -x -> extract files from archive.
        - -j -> Decompress with bzip2 command
        - -f ARCHIVE : operates on the archive file.
        * It is important to keep the -f flag at last or esle terminal will show error as no such directory because it expects the directories after -f flag mandatorily.
        - example - tar -xjf folders.tbz
    
    - __Zip files__ : The command for using comopressing a file using zip is - 
        - zip [OPTIONS] [zipfile [file…]] : example : zip alpha_files.zip alpha*
        - zip will not recurse to the subdirectories like tar to achieve this you may use -r option in zip.
        - To unzip a file - unzip [zipped_filename] 