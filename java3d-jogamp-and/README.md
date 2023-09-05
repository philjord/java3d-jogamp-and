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