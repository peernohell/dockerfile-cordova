This is an extention to ahazem/android that add npm and cordova

to simplify use you can add this alias to your bashrc/zshrc

```
alias cordova='docker run --rm -i -v `pwd`:/workspace -w /workspace peernohell/cordova cordova'
```

after you will be able to call cordova on the docker as if is called from your shell.

```
~/projects$ cordova create hello com.example.hello HelloWorld
Creating a new cordova project with name "HelloWorld" and id "com.example.hello" at location "/workspace/hello"
Downloading cordova library for www...
Download complete

~/projects$ ls
hello/

~/projects$ cd hello/

~/projects/hello$ cordova platform add android
Downloading cordova library for android...
Download complete
Creating android project...
Creating Cordova project for the Android platform:
Path: platforms/android
Package: com.example.hello
Name: HelloWorld
Android target: android-19
Copying template files...
Running: android update project --subprojects --path "platforms/android" --target android-19 --library "CordovaLib"
Resolved location of library project to: /workspace/platforms/android/CordovaLib
Updated and renamed default.properties to project.properties
Updated local.properties
No project name specified, using Activity name 'HelloWorld'.
If you wish to change it, edit the first line of build.xml.
Added file platforms/android/build.xml
Added file platforms/android/proguard-project.txt
Updated project.properties
Updated local.properties
No project name specified, using project folder name 'CordovaLib'.
If you wish to change it, edit the first line of build.xml.
Added file platforms/android/CordovaLib/build.xml
Added file platforms/android/CordovaLib/proguard-project.txt

Project successfully created.

```
