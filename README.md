# SQLCipher for Android: the Artifact

**NOTE**: The official AAR is now available from JCenter via `compile 'net.zetetic:android-database-sqlcipher:3.3.1-1@aar'`. Please use it. This artifact is officially deprecated, replaced by the official one.

[SQLCipher](https://www.zetetic.net/sqlcipher) is an encrypted
edition of SQLite.
[SQLCipher for Android](https://www.zetetic.net/sqlcipher/sqlcipher-for-android/)
is a port of that SQLite to Android, complete with a JAR that
offers an API mirroring that of Android's native SQLite API.

At the present time, though, SQLCipher for Android is not
available as an official artifact from [Zetetic](https://www.zetetic.net).
The official distribution is in the form of a ZIP archive
that you have to (carefully) unpack into the right spots in your
project and, in the case of Android Studio, add (carefully)
to your `build.gradle` file.

This GitHub repo represents a packaging of the SQLCipher for
Android distribution in a standard Android library module.
In addition, that library is distributed as an AAR for easier
integration into an Android Studio project.

However, it should be noted that **this is totally unofficial**.
It is hoped that Zetitec will distribute an AAR via an artifact
repository themselves someday, at which point
**this project will become officially deprecated**.

Installation
------------
To integrate the AAR, add the following closures to your
module's `build.gradle` file:

```groovy
repositories {
    maven {
        url "https://repo.commonsware.com.s3.amazonaws.com"
    }
}

dependencies {
    compile 'com.commonsware.cwac:sqlcipher-for-android:3.3.1'
}
```

From there, you use SQLCipher for Android the same way that you
would if you were using the official ZIP file distribution.

Note that the version number of the artifact will mirror
the version number of the official SQLCipher for Android distribution.

Demo
----
There is a `demo/` module, alongside the library module. Mostly,
the demo module is there to confirm that the library module
itself is working fine. You're welcome to poke at the code for
the demo module to see how to use SQLCipher for Android in a very
crude form. In particular, note that while the demo module uses
a hardcoded passphrase, nobody
ships a production-grade app using a hardcoded passphrase.

License
-------
Please read [Zetitec's README for licensing information](https://github.com/sqlcipher/android-database-sqlcipher#license)
for SQLCipher for Android itself.

The demo module and ancillary project files unique to this
repo are licensed under the Apache Software License 2.0.

Questions
---------
Quoting Zetetic, "the primary venue for free support and
announcements is [the SQLCipher discuss site](https://discuss.zetetic.net/category/sqlcipher)."
You can read more about SQLCipher for Android's support
options on [the SQLCipher support page](https://www.zetetic.net/sqlcipher/support/).

If you are encountering problems *specifically* with this
artifact (not SQLCipher for Android itself), you can
file [an issue](issues).

Release Notes
-------------
- 3.3.1: initial release of artifact
