This project was converted to Android Studio V1.5 and Gradle in version 2.11.13.  The new build system have a different file structure that Eclipse had.  Gradle also is very different than how builds were handled in Eclipse.  

There is a missing file you need in the app folder called build.gradle.  You will need to create this file and set up the versions and dependencies as follows.

`apply plugin: 'com.android.application'
android {
signingConfigs {
config {

    }
}
compileSdkVersion 19
buildToolsVersion '23.0.2'
defaultConfig {
    applicationId "a2dp.Vol"
    minSdkVersion 15
    targetSdkVersion 19
}
buildTypes {

}
sourceSets {
    main {
        manifest.srcFile 'src/main/AndroidManifest.xml'
    }
}
}

dependencies {
compile 'com.android.support:support-v4:21.0.3'
}`