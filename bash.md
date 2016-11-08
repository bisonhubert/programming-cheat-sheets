# Bash Cheat Sheet

- [Locating Files](#locating-files)
- [Listing Processes](#listing-processes)
- [Killing Processes](#killing-processes)
- [Run Process in Background](#run-process-in-background)
- [Xcode](#xcode)

### Locating Files
```bash
find all files with .txt extension
$ find . -type f -name "*.txt"
```

```bash
find all directories with .app extension
$ find . -type d -name "*.app"
```bash


### Listing Processes
```bash
list all processes
$ ps
```

```bash
list processes, including those run outside terminal
$ ps
```

```bash
list processes by name
$ ps -e | grep <process-name>
```

```bash
list jobs running in terminal window / tab
$ jobs -l
```


### Killing Processes
```bash
after finding the PID of the process
$ kill <process-id#>
```


### Run Process in Background
```bash
$ npm start &
```

### Android
```bash
list android SDKs
$ ls /Users/bisonwithpillow/Library/Android/sdk
```


### Xcode

```bash
path to
$ xcode-select --print-path
```

```bash
switching versions
$ sudo xcode-select -switch /Applications/<version>
```
