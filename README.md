# wcwidth() Implementation in Swift for OS X

wcwidth() is an important function when writing command line tools. However, the wcwidth() function shipped in OS X is old. A lot of characters added in newer versions of Unicode are not supported. In contrast, the glibc implementation of Linux is much more updated. This project aims to provide a modern implementation of wcwidth() in OS X. This implementation uses a 3-level compact array to reduce the usage of memory and improve the lookup speed. Each lookup only takes constant time.

# API

* `func characterWidth(codePoint: Int) -> Int`

  Return the number of columns required to display the Unicode character represented by the given code point.

# See Also

* [Unicode Demystified: A Practical Programmer's Guide to the Encoding Standard](http://www.amazon.com/Unicode-Demystified-Practical-Programmers-Encoding/dp/0201700522)
* [Bits of Unicode - Macchiato](http://macchiato.com/slides/Bits_of_Unicode.ppt)
