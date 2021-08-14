- Take an arbitrary numeric address as input!!!

- Write byte order getopt code for all functions
  * like currently existing `-o` for _rev_

- Include a getopt flag to perturb normal output
  * 0x7f.0x0.0x0.0x1 vs. 0x7f.0x00.0x00.0x01
  * 0x7f.0x0.0x0.0x1 vs. 0x7f.0x00.0x0.0x1
  * etc.

- Make sure these from research are implemented
  * https://hackerone.com/reports/128685
  * AppSecEU15 - Server side browsing considered harmful
    - note that it combines multiple formats in one address

- Write warnings to stderr for invalid address
  * for example, `$ inet2hex 256.256.256.256 => 0x100100100100`
