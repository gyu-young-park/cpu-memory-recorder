# Linux CPU-Memory Recorder
This is for recording CPU and memory usage in linux server. This program records CPU and memory usage at interval of some second(**default 3s**). And output file will be generated in current folder, the file name is 'cpu-mem.csv'. If you want to change output file name or path, you can change by option(`-o`). 

The Output shcema is `csv`, Please refer to below
```
date(MM-DD-hh-mm-ss),cpu-usage,memory-usage
```

- example)  
```
11:03:14:59:10,1.07,38.91
```

# How to use

## Start
```sh
./cpu_memory_recorder.sh
```

## Option
There are two options. The One is output file path, the other is interval of recording.
```
./cpu_memory_recorder.sh -o {file-path} -i {interval}
```

You can use help option(`-h`). It provide how to use this program
```
./cpu_memory_recorder.sh -h

Usage: ./cpu_memory_recorder.sh -o ./cpu-mem.csv | -i 10
        -o Output file path.                   ex) -o ./cpu-mem.csv
        -i Recording interval time(second).    ex) -i 10
Output Data format is csv please check below
------------------------------------------------
DATE           | CPU USAGE     | MEMORY USAGE  |
11:03:14:59:10 , 1.07          , 38.91         |
------------------------------------------------
```

## Note!
When the program starts, program Automatically try to remove output-file.   