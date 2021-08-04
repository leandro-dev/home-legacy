Leandro's Home
==================

Project to start my home automation. 

In the first step, I want to setup an integration with Raspberry Pi to water my plants.

I also want to use this project to test some new technologies and to be my showcase.

Irrigation system
-----------------
This project can be divided in some parts:

- Control the Raspberry Pi board (hopefully with kotlin multiplatform + nodejs) to trigger the watering system.
- Monitor the status and history for every plant with an Android app. Maybe in the future I can build an iOS project with kotlin MPP.
- Configure plant and sensors registration with Firebase console.

Quick Overview
--------------
![Icon (1)](https://user-images.githubusercontent.com/1706622/128160651-e2377574-d79b-4a99-90e7-f8b5b9b97304.png)

I would like to apologize for my terrible design skills, but I hope you got the references from the icon :)

Here it is a quick intro of how simple this project will be, just 2 screens to start, just a list of plants with a detail screen
![image (10)](https://user-images.githubusercontent.com/1706622/128160876-95b193f3-3a30-4abd-9ad5-11cb2c5d23aa.png)


Architecture
------------

Modularization
--------------

As the usual projects of large companies tend to grow quickly, this project will be heavily based on modularization with demo-apps.

The idea behind a module called demo-app is to enable developers to quickly test a module, without having to build the entire project to test a specific change.

If this project grows larger, it will be worthy to split each module into public/private modules, in order to help dependencies to provide a custom fake-implementation of the public interface definition.

Libraries Used
--------------
* UI
  * [Jetpack Compose][1] - It will require **Android Studio Arctic Fox**.
* Data Sources
  * [Ktor-Client][2] - A multiplatform asynchronous HTTP client
  * [Firestore][3] - NoSQL cloud database
* Third party and miscellaneous libraries
  * [Hilt][4]: Dependency injection in Android
  * [Navigation][5] - Jetpack Compose Navigation
  * [Coroutines][6] - Asynchronous code in a sequential fashion
  * [Kotlix-Serialization][7]: Convert between trees of objects and strings, byte arrays, etc.
* Tests
  * UI
    * [Compose Layout][8]: Testing compose layouts

Future concerns
---------------
This is more than enough to start working in this project. If it gets to a point where other people can use it, I'll start worrying about topics related to CI/CD, Crash Monitoring, Analytics, etc.


[1]: https://developer.android.com/jetpack/compose
[2]: https://ktor.io/docs/getting-started-ktor-client.html
[3]: https://firebase.google.com/docs/firestore
[4]: https://developer.android.com/training/dependency-injection
[5]: https://developer.android.com/jetpack/compose/navigation
[6]: https://kotlinlang.org/docs/coroutines-overview.html
[7]: https://github.com/Kotlin/kotlinx.serialization/blob/master/docs/serialization-guide.md
[8]: https://developer.android.com/jetpack/compose/testing
