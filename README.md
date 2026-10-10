# xsun

A copy of internal `sun` APIs (only JVM-independent parts).

This repository primarily contains things I bothered to port because I personally need it.

The original source code is available at <https://github.com/openjdk/jdk/tree/master/src/java.base/share/classes/sun>
and the code in this repository is available under the same exact license.

## Modifications done to sun

For anything copied, we are renaming the package from `sun` to `xsun` and removing the use of any internal APIs.
Because of this, the behavior may differ:

- In `IPAddressUtil#invalidIpAddressLiteral` uses of `formatMsg` and `filterNonSocketInfo` were replaced with basic
  string concatenation. Exception messages may differ.

## Contributing

As this is strictly a copy of `sun`, we do not accept any feature requests. We may accept security patches if
necessary, but staying the same.

Only copy files from <https://github.com/openjdk/jdk/tree/master/src/java.base/share/classes/sun> and make sure that
no internal OpenJDK (or others) APIs are used.