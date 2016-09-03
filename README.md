# HaarCascadeTraining
Learning how haar cascade works in OpenCV. Training to detect cars in real time. Overall goal is to be able to detect vehicles and lanes while driving by utilizing the phone camera.

## Dependencies

[OpenCV Android 3.1](http://opencv.org/downloads.html)

[Android Studio 2.1](https://developer.android.com/studio/index.html)

[OpenCV Haar Cascade Face Detection Example](http://docs.opencv.org/trunk/d7/d8b/tutorial_py_face_detection.html)

[Android NDK Bundle (allows application developers to build performance-critical portions of their apps by use of native (C/C++) code)](https://developer.android.com/ndk/downloads/index.html)

[Positive Car Rear Images Dataset](http://lars.mec.ua.pt/public/Media/ResearchDevelopmentProjects/HaarFeatures_RoadFilms/HaarFeaturesTests/CarsRear/)

This setup is to support Android Marshmallow 6.0.1 (API 23) and testing is being done on Samsung Galaxy S7 edge.

## Configurations

In the app build.gradle, targetSdkVerison.apiLevel is set to 22 because with API 23, you need to request permissions to access and use the camera. Setting target API to 22 allows us to still use the camera without needing to explicitly request camera permission.
>targetSdkVersion.apiLevel = 22

Android NDK Settings
> Flags for c++ compiling. Settings are found in app's build.gradle under android.ndk
```
cppFlags += "-std=c++11"
cppFlags += "--debug"
cppFlags += "-frtti"
cppFlags += "-fexceptions"
```

## Todo
```
Determine success rate of detection.
Figure out best way to detect traffic lanes.
Implement both to detect simultaneously
```


## License
[GNU License](https://github.com/gentlespoon/rshell/blob/exec/LICENSE)
