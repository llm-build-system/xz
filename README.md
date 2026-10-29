# XZ Utils / liblzma - llm port

Original project: [XZ Utils / liblzma](https://github.com/tukaani-project/xz), version 5.8.4.
Original authors: Lasse Collin and the XZ Utils contributors, with LZMA code based on Igor Pavlov's LZMA SDK and SHA-256 code based on Wei Dai's Crypto++. [Original repository](https://github.com/tukaani-project/xz).

The library is the work of its original authors, not a product of llm-build-system.
This repository only maintains its llm build integration and source subset.
It is not an official upstream release. Upstream source and header files are
unchanged. Build configuration files added by this port are kept separately.
Upstream build systems, command-line tools, tests and manuals are omitted.

The original license is preserved verbatim in [LICENSE](LICENSE).
[Upstream license](https://github.com/tukaani-project/xz/blob/v5.8.4/COPYING.0BSD). Copyright and per-file license notices
remain in the original files.

Build the static liblzma library with `llm build --release`. Consumers include
`<lzma.h>`. All upstream encoders, decoders, BCJ filters and checks are
enabled, including multithreaded compression/decompression. This port uses
portable C implementations rather than optional architecture-specific
assembly/CRC intrinsics. Only the 0BSD-licensed library subset is included.
GPL/LGPL command-line tools and build machinery are omitted.
