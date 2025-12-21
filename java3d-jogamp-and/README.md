Java3D Jogamp Android Readme
===
This code is a collection of altered java classes that override those in the org.jogamp.jogl-all-android project to fix bugs, extend debugging and include the native libraries.

I cannot for the life of me get Android Studio to include the .so files as deployed by Jogamp

Note the .so files are taken from the *-android-* jar file, not the fat jar

So arm64-v8a comes from native folder in 

gluegen-rt-android-natives-android-aarch64.jar

joal-natives-android-aarch64.jar

jogl-all-android-natives-android-aarch64.jar

and armabi-v7a comes from native folder in 

gluegen-rt-android-natives-linux-amd64.jar

joal-natives-linux-amd64.jar

jogl-all-android-natives-linux-amd64.jar


Notes on compiling, this project compiles against an android hybrid jdk, built out of 1.8.0_66, with the android.jar and a whole bunch of andoirdx jars added called jdk1.8.0_66a

This hybrid jdk is held in a zip file 

This compile JDK sometimes gets the extra android jar removed by the IDE randomly so needs them re-added under the edit of Installed JRE's

Also this compile JDK can't be used to run any maven builds or install, so you must run as... Maven build... and set the JRE tab to use JDK 11 not the project default

On the same note, your maven run as MUST have a JAVA_HOME variable set in the "Environment" tab of the latest jdk if you want javadocs to build

Note on how to upgrade jogl version, recompare the source with these overrides and update. Also get the new android libs from here, and all the other similar sub parts

https://repo1.maven.org/maven2/org/jogamp/jogl/jogl-all-mobile/x.x.x/

https://repo1.maven.org/maven2/org/jogamp/gluegen/gluegen-rt-android/2.6.0/

https://repo1.maven.org/maven2/org/jogamp/joal/joal-android/2.6.0/

into

C:\Users\pjnz\git\java3d-jogamp-and\java3d-jogamp-and\libs\lib\arm64-v8a