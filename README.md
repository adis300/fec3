# Original source page:

[http://www.ka9q.net/code/fec/](http://www.ka9q.net/code/fec/)
* [Home](http://www.ka9q.net)
* [Code](http://www.ka9q.net/code)
* [DSP and FEC Library](http://www.ka9q.net/code/fec/)



# DSP and FEC Library

[fec-3.0.1.tar.bz2](http://www.ka9q.net/code/fec/fec-3.0.1.tar.bz2) (7 August 2007)

This library package provides several forward error correction (FEC) decoders and accelerated primitives useful in digital signal processing (DSP). Except for the Reed-Solomon codecs, these functions take full advantage of the MMX, SSE and SSE2 SIMD instruction sets on Intel/AMD IA-32 processors and the Altivec/VMX/Velocity Engine SIMD instruction set on the G4 and G5 PowerPC.

Version 3.0.1, released 7 August 2007, fixes a bug in the CCSDS Reed-Solomon encoder.

The new Intel Macs are not yet supported. Stay tuned.

The library includes Viterbi decoders for the following convolutional codes:

* rate 1/2 k=7
* rate 1/2 k=9
* rate 1/3 k=9
* rate 1/6 k=15 ("Cassini")

plus two Reed-Solomon encoder-decoders:

* one optimized for the (255,223) CCSDS standard code
* a general purpose encoder/decoder for arbitrary RS codes


and three low-level 16-bit DSP support routines:

* signed dot product
* peak detection
* sum-of-squares (energy) computation


This library is licensed under the "lesser" GNU General Public License.

# Older FEC Software

## Optimized Reed-Solomon encoder/decoder with x86asm assist for (255,223) code on Intel CPUs

This is older code without CCSDS support. It is not yet integrated into the fec library above.
* [readme file](http://www.ka9q.net/code/fec/rs32readme.txt)
* [source, gzipped tar](http://www.ka9q.net/code/fec/rs32.tar.gz)

## C++ class library for galois field arithmetic and algebra, with RS encoder/decoder

This is a class library for doing finite field arithmetic and algebra over GF(256). Two classes are defined: galois and polynomial, implementing galois field elements and polynomials over galois field elements, respectively. A (255,223) Reed-Solomon encoder and decoder functionally equivalent (but much slower than) my C version is included to demonstrate the use of the library. Because of its slow speed, the C++ version is primarily intended for educational use; it was my first non-trivial C++ program. (This version doesn't do the CCSDS standard).
* [source, gzipped](http://www.ka9q.net/code/fec/galois.tar.gz)

## Convolutional (Fano) decoder, version 1.1

* [source, gzipped tar archive](http://www.ka9q.net/code/fec/fano1.1.tar.gz)
Last modified: 7 August 2007