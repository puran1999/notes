This is how I wanted:
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

MPLAB only shows a file if it is created within MPLAB.
MPLAB will not create file outside project folder.
MCC creates all files including main.c in src(1) folder.
If Keeping include files in src(1), files are unavailable in MPLAB, project *might* build successfully

