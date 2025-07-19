This is the file structure I wanted:
```C
RBT Cleaner V5.0
├───RBT Cleaner V5.0.X
└───src
    ├───main.c
	├───rtc_ext.c
	├───rtc_ext.h
    └───config
        └───default
            └───peripheral

```
This is what I get:
```C
RBT Cleaner V5.0
├───RBT Cleaner V5.0.X  //(MPLAB cannot generate files outside this folder)
│   └───src(2)
│		└───rtc_ext.c
│		└───rtc_ext.h
└───src(1)  //(This folder is created by MCC)
    ├───main.c
    └───config
        └───default
            └───peripheral  //(This folder has all MCC libraries (UART, etc))
```
Problem:
MPLAB only shows a file if it is created within MPLAB.
MPLAB will not create file outside project folder.
MCC creates all files including main.c in src(1) folder, which is out of the scope of MPLAB.
If Keeping include files in src(1), files are unavailable in MPLAB, project *might* build successfully.
If Keeping a dummy `main.c` file in src(1) and actual file in src(2), project still builds, but it is confusing.

So now only way seems to be following this folder structure and including files like this in `main.c`:
```C
#include "../RBT Cleaner V5.0.X/src/rtc_ext.h"
```

That is what I am doing now, will focus more on code, because this issue can be resolved in future also, no changes required on coding side.
