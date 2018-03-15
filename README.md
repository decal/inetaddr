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

* * * 

# Demonstration of each function

``` bash
$ cat test-inetaddr
#!/usr/bin/env bash
#
# Test functions implemented by inetaddr script
#
# Written by Derek Callaway <decal@sdf.org>
# Wed May 31 06:23:11 PDT 2017
#

source inetaddr

inet2oct 127.0.0.1
decq2oct 127.0.0.1
inet2hex 204.79.197.200
decq2hex 204.79.197.200
inet2dec 192.168.1.1
decq2dec 192.168.1.1

inet2octq 172.16.0.1
decq2octq 10.10.10.10
inet2hexq 8.8.4.4
decq2hexq 255.255.255.255

octq2inet 0172.0.0.1
octq2decq 0172.0.0.1
hexq2inet 0x7f.0x0.0x0.0x1
hexq2decq 0x7f.0x0.0x0.0x1

hex2inet 0x01010101
hex2decq 0x01010101
dec2inet 3232235777
dec2decq 3232235777
oct2inet 017700000001
oct2decq 017700000001

hexq2octq 0x7f.0x0.0x00.0x01
octq2hexq 0172.0.0.01

exit 0
$ ./test-inetaddr
017700000001
017700000001
0xcc4fc5c8
0xcc4fc5c8
3232235777
3232235777
0254.020.00.01
012.012.012.012
0x08.0x08.0x04.0x04
0xff.0xff.0xff.0xff
122.0.0.1
122.0.0.1
127.0.0.1
127.0.0.1
1.1.1.1
1.1.1.1
192.168.1.1
192.168.1.1
127.0.0.1
127.0.0.1
0177.00.00.01
0x7a.0x00.0x00.0x01
```
