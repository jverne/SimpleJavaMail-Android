# SimpleJavaMail-Android
Android port of [SimpleJavaMail](http://www.simplejavamail.org/) to bring fluent JavaMail functionality to Android API 17 or greater.

Initial port:

- Exclude Spring support
- Force using the Sun/Oracle [android-mail and android-activation](https://javaee.github.io/javamail/Android) libraries at specific versions, and exclude any refs to `javax.mail` or `javax.activation` from other transitive dependencies
- Create local version of `StandardCharsets` to satsify missing symbols in Dalvik
- Create a `ReusableCountLatch` to remove depencency on Java Phasers, also missing in Dalvik

