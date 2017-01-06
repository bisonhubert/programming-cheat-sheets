# Bash Cheat Sheet

- [Locating Files](#locating-files)
- [Listing Processes](#listing-processes)
- [Killing Processes](#killing-processes)
- [Run Process in Background](#run-process-in-background)
- [Version Management](#version-management)
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

### Version Management
```bash
set version of Node with nvm
$ nvm alias default v5.0.0
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

```bash
create a build of a project (in progress)
$ xcodebuild -project ios/pro_mobile.xcodeproj -target pro_mobile.app
```

```bash
list all targets, build configurations, and schemes used in project
$ xcodebuild -list -project <project-name>.xcodeproj
```






### Android

```bash
list android SDKs
$ ls /Users/bisonwithpillow/Library/Android/sdk
```

```bash
start emulator
$ emulator -avd <name> -gpu on &
```

```bash
list virtual devices
$ android list avd
```

```bash
delete emulator
$ android delete avd -n <name>
```

```bash
install android-21 google abi
echo y | android update sdk --no-ui --all --filter addon-google_apis-google-21
echo y | android update sdk --no-ui --all --filter sys-img-armeabi-v7a-google_apis-21
$
```

```bash
create new emulator
$ echo no | android create avd --name "TTTest" --target "android-22" --abi "google_apis/x86" -s "1440x2560" --device "Nexus 6" -c 128M
```

```bash
list targets
$ android list targets
```

CREATE
echo no | android "create" "avd" "--force" "--name" "test" "--target" "android-21" "--abi" "armeabi-v7a"

START
emulator -avd test -skin 768x1280 -no-boot-anim -no-audio


API 24 from Google
set -ex
echo y | android update sdk --no-ui --all --filter addon-google_apis-google-22
echo y | android update sdk --no-ui --all --filter sys-img-armeabi-v7a-google_apis-22
echo no | android create avd --force --name test --target "android-22" --abi "google_apis/x86


STARTING

BITRISE default
-avd <name> -skin 768x1280 -no-boot-anim -no-audio -no-window

BITRISE edits
-avd test -skin 1440x2560 -no-boot-anim -gpu on &
