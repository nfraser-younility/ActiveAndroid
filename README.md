# ActiveAndroid-Secure

This adds SQLCipher support to ActiveAndroid. It's mostly just a re-implementation of [ActiveAndroid-Secure](https://github.com/zsiegel/ActiveAndroid-Secure) on top of the latest ActiveAndroid, adding a method to set the password separately.

The included `sqlcipher.jar` comes from `classes.jar` in the [SQLCipher for Android 3.3.1-2 .aar binary package](https://www.zetetic.net/sqlcipher/sqlcipher-for-android/). It is only needed to allow the compiler to find SQLCipher classes when building ActiveAndroid. The resulting `ActiveAndroid.jar` does not include SQLCipher.

To use this in a project, build this to produce `ActiveAndroid.jar`, add it to your app's `libs/`, and add a SQLCipher dependency to your project. Like this:

```groovy
dependencies {
    compile fileTree(include: ['*.jar'], dir: 'libs')
    compile 'net.zetetic:android-database-sqlcipher:3.3.1-2@aar'
}
```
