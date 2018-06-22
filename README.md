Helper project to create an empty JAR with a `Class-Path` attribute.

This is useful for testing gosu-lang/gosu-lang#138

**Steps to reproduce:**

1. `$ ./gradlew jar`
2. `$ gosu -classpath build/libs/gosu-lang-138.jar RunMe.gsp`

Expected output: `org.junit.runner.Computer@<randomdigits>`

Note that the location of `gosu` executable in step 2 is likely not on the PATH; most likely you'll want to use a fully-qualified path to the executable.

**Pursuant to the [JAR specification](https://docs.oracle.com/javase/7/docs/technotes/guides/jar/jar.html#Main_Attributes), the `Class-Path` attribute must be a space-delimited list of URLs.**