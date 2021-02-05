The Freetype font rasterizer in the Go programming language.

This version has modifications by
[onioneffect on GitHub](https://github.com/onioneffect)! See changes at the end of this file!

To download and install from source:
$ go get github.com/golang/freetype

It is an incomplete port:
  * It only supports TrueType fonts, and not Type 1 fonts nor bitmap fonts.
  * It only supports the Unicode encoding.

There are also some implementation differences:
  * It uses a 26.6 fixed point co-ordinate system everywhere internally,
    as opposed to the original Freetype's mix of 26.6 (or 10.6 for 16-bit
    systems) in some places, and 24.8 in the "smooth" rasterizer.

Freetype-Go is derived from Freetype, which is written in C. Freetype is
copyright 1996-2010 David Turner, Robert Wilhelm, and Werner Lemberg.
Freetype-Go is copyright The Freetype-Go Authors, who are listed in the
AUTHORS file.

Unless otherwise noted, the Freetype-Go source files are distributed
under the BSD-style license found in the LICENSE file.

## Changes:
* Modify `freetype.go` to add functions `StrAdvanceWidth` and `StrAlign`.
* Add example `freetype/advance` to demonstrate how to calculate the advance
width of a string.
* Add example `freetype/align` to demonstrate `StrAlign`.

Important note: The examples that I made include
`"github.com/onioneffect/freetype"`, while the original examples include
`"github.com/golang/freetype"`. Only the former has the changes listed above!
