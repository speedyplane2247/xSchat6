# List of versions
Here's a cool little list of versions. These are ordered by date, and I started using the 1.x architechture again, but the 1.0.x & 1.1.x are the latest.

## v0.9.0
Simple plain-text with header parsing.
## v1.0.0
Simple base64 encoding.
## v2.0.0
Multi-layer Base64 with header support.
## v2.1.0
Multi-layer Base64 without header support for stability.
## v3.1.0
Re-introduced header support & footer support.
## v3.1.3
Added compatibility mode, to view both 0.9, 1.0, and 2.x seemlessly. This build is the final "legacy" build, supports pretty much all versions prior.  
## v4.0.0
This introduces a brand new algorithm, without header support as of release.
## v4.1.0
This adds basic header support.
## v4.2.0
This adds more advanced header support, and a basic footer. 
## v4.2.1
This, unsuprisingly, introduces better footer support.
## v4.2.2
This a pretty advanced bug patch, and is suited as the final release of the new 4.x project. The 4.x project was VERY stable, and used for quite a while.
### Leakage
This build was accidently leaked while giving a user a demo build, and the actual decryption / encryption engine was leaked, and easily reverse-engineered and then published, which resulted in a new algorithm having to be made, as 4.2.3 could be easily patched with the new keys from the read-only variant.
## v4.2.3
4.3.2 was a quickly released hot-fix that tried to fix the leakage of 4.2.2, but it didn't really work as the engine stored an internal key that could be used to generate the standard key as a fail-safe to help secure data transmission.
## v5.0.0
5.0.0 was the true fix to 4.2.2 being leaked, as the engine is nearly the same as 4.2.2, but with a larger key size, pre-obfuscated, and without the key recovery functions. It was pretty buggy, as the keygen for it wasn't very good.
## v5.0.1
5.0.1 was one of the most the most inconsistent releases, with some people's copies running just fine, both the encryption and decryption engines running without problems, while others broke the decryption engine.
## v5.0.2
5.0.2 introduced a status checker, as it came out while 1.0.2 was in RC stages. It doesn't support 5.0.1 / 5.0.0 headers, and is modified to not be able to be read by 5.x. Interestingly enough, this can not only read 4.2.0 builds, but also can be read by, as a typo in the code is looking for NOT 5, and REQUIRE 0 & 2. 
### Time Lock
When 5.0.2 was released, it was planned to make the buggy, and inflated codebase of 5.x not work anymore, and included a free upgrade to 1.0.2 and 1.1.0, as 5.0.2 won't start if it can't reach the server. This can't be bypassed, as part of the engine was stored on the server, and no caches were made.
### "Final" of the Series
5.0.2 was the final of the pretty unsuccessful 5.x series, which was made as a fix for the very successful 4.x, specifcally th now leaked 4.2.2 codebase, after 4.2.3 failed. Full of bugs, it was decided that 6.x was required.
## 6.0.0
6.0.0 was never released, but it was another attempt at a 4.2.2 fix. It was obviously disconitnued, but it was a direct fork of 4.2.2, without obfuscation, and no key recovery. In testing, the UI wasn't very friendly, and it was very bulky to work with another UI, so it was scrapped in favor of 1.0.2. This brings the 1.0 codebase to the 2.1 multi-encoder support to the mainstream, with support for 1.0, 2.x, 3.x, 4.x, and 5.0.0.
## v1.0.2
v1.0.2 is a much different version of base64, encoding multiple times. This version of the engine is still in decently heavy use, so the code isn't released. It has compatibility for various previous versions.
## v1.0.2-ghc
The 'ghc' branch is for github, and has variations in the amount of encoding/decodings. This also doesn't have some modifications that seperate the two.
## v1.1.0
This build is the latest engine, and includes a new header format.
