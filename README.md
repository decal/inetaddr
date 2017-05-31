# IPv4 address format conversion functions for bash

* `inetaddr` is the script which contains function definition source code
* `test-inetaddr` contains statements that test each individual function

## Names, descriptions and aliases of functions provided by `inetaddr`

The name of each function describes what format it takes as input as well as
what format it intends to produce as output. The strings `dec`, `hex` and `oct`
respectively represent the **decimal**, **hexadecimal** and **octal** numbering 
systems. A dotted-quad is being described when a _q_ appears on the end. For
example, `inet2hexq` converts a typical numeric IPv4 Internet address to a 
dotted-quad format of hexadecimal values. The various function aliases that
are available provide identifiers that replace the string `inet` with `decq` for
convenience, as an IPv4 Internet (_inet_) address is also a dotted-quad of 
decimal values (_decq_.) Refer to 
[Dot-decimal notation - Wikipedia](https://en.wikipedia.org/wiki/Dot-decimal_notation)
for more information on the dotted-quad style of IPv4 Internet addresses. 

* `inet2dec` - dotted-decimal-quad to a single decimal value
* `inet2hex` - dotted-decimal-quad to a single hex value
* `inet2oct` - dotted-decimal-quad to a single octal value

* `dec2inet` - single decimal value to dotted-decimal-quad
* `hex2inet` - single hex value to dotted-decimal-quad
* `oct2inet` - single octal value to dotted-decimal-quad

* `inet2hexq` - dotted-decimal-quad to dotted-hex-quad
* `inet2octq` - dotted-decimal-quad to dotted-octal-quad

* `hexq2inet` - dotted-hex-quad to dotted-decimal-quad
* `octq2inet` - dotted-octal-quad to dotted-decimal-quad

* `octq2hexq` - dotted-octal-quad to dotted-hex-quad
* `hexq2octq` - dotted-hex-quad to dotted-octal-quad
