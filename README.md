# SimpleJavaMail-Android
Android port of [SimpleJavaMail](http://www.simplejavamail.org/) to bring fluent JavaMail functionality to Android API 17 or greater.

Initial port:

- Exclude Spring support
- Force using the Sun/Oracle [android-mail and android-activation](https://javaee.github.io/javamail/Android) libraries at specific versions, and exclude any refs to `javax.mail` or `javax.activation` from other transitive dependencies
- Create local version of `StandardCharsets` to satisfy missing symbols in Dalvik
- Borrow and modify a `ReusableCountLatch` to remove depencency on Java Phasers, also missing in Dalvik

# TODO
- Actually publish to this placeholder
- Figure out how to pull and patch upstream changes, as we can't (or, rather, don't get any value from) just forking
    - Perhaps this up as flavors so we keep the official release in one source tree and copy and patch to build the actual Android flavor
- Get tests working
