# WEEK 3 LAB REPORT #

## FIND COMMAND ##

### Partial Name Search ###

```find [path] -iname [text]``` will search for the text entered as an approximate file name; meaning it will return any files containing "text," non-case sensitively. This is useful in case you don't remember the name of a file exactly, or are looking to pull up multiple related files (for example, all files about Hong Kong).

Searching for any text files containing "hongkong:"
```
$ find written_2/ -iname "*hongkong*.txt"
written_2//travel_guides/berlitz1/HandRHongKong.txt
written_2//travel_guides/berlitz1/HistoryHongKong.txt
written_2//travel_guides/berlitz1/IntroHongKong.txt
written_2//travel_guides/berlitz1/WhatToHongKong.txt
written_2//travel_guides/berlitz1/WhereToHongKong.txt
```

Searching for any text files containing "madrid:"
```
$ find written_2/ -iname "*madrid*.txt"
written_2//travel_guides/berlitz1/HistoryMadrid.txt
written_2//travel_guides/berlitz1/IntroMadrid.txt
written_2//travel_guides/berlitz1/HandRMadrid.txt
written_2//travel_guides/berlitz1/WhereToMadrid.txt
```

### Search by Type ###
```find [path] -type [f/d]``` will search for only a specified type of file; you can limit results to only files, only directories, etc. This is useful if you are looking to only search for a certain type of item within a directory; perhaps you only want other directories or files.

Searching for only directories:
```
$ find written_2/ -type d
written_2/
written_2//non-fiction
written_2//non-fiction/OUP
written_2//non-fiction/OUP/Berk
written_2//non-fiction/OUP/Abernathy
written_2//non-fiction/OUP/Rybczynski
written_2//non-fiction/OUP/Kauffman
written_2//non-fiction/OUP/Fletcher
written_2//non-fiction/OUP/Castro
written_2//travel_guides
written_2//travel_guides/berlitz1
written_2//travel_guides/berlitz2
```

Searching for only files starting with "Beijing:"
```
$ find written_2 -type f -name "Beijing*"
written_2/travel_guides/berlitz2/Beijing-History.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
```

### Limit Depth of Results ###
```find [path] -maxdepth [depth]``` will search only within a given depth. This is useful if you are looking to only search within x number of directories within a given path, if you don't want to look recursively into every single one available

Searching for files with a depth of 1:
```
$ find written_2/ -maxdepth 1
written_2/
written_2//non-fiction
written_2//.DS_Store
written_2//travel_guides
```

Searching for files with a depth of 2:
```
$ find written_2/ -maxdepth 2
written_2/
written_2//non-fiction
written_2//non-fiction/OUP
written_2//.DS_Store
written_2//travel_guides
written_2//travel_guides/.DS_Store
written_2//travel_guides/berlitz1
written_2//travel_guides/berlitz2
```

### Search for a path ###
```find [path] -ipath [text]``` will search for a file and return the path leading to it. This is useful if you know what file you're looking for, but perhaps don't know the path to find it exactly.

Searching for path of Bahamas-History.txt:
```
$ find written_2/ -ipath "*Bahamas-History.txt"
written_2//travel_guides/berlitz2/Bahamas-History.txt
```

Searching for path of berlitz1:
```
$ find written_2/ -ipath "*berlitz1"
written_2//travel_guides/berlitz1
```

*All commands found on [https://www.redhat.com/sysadmin/linux-find-command]([https://www.google.co](https://www.redhat.com/sysadmin/linux-find-command)*
