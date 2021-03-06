# Principles of stax

Here are the basic design principles of stax.  Subject to change at my whim, but rarely have so far.

 1. No non-determinism.  That includes `today()` type functions and `random(max)` or `choice(list)` type functions as well.  I think when non-determinism is allowed in golf, it tends to degenerate into philosophical arguments.  That's all well and good if that's your thing, but not where stax is going.
 1. No dates or date-related features.  Stax is supposed to "fun".  I get more than enough date stuff in real work.
 1. For new language feature consideration, the feature must be able to demonstrate superiority.  There must be some kind of vaguely plausible golf challenge which it can solve shorter than existing language features.
 1. For new language feature consideration, the size of the brevity of programs is paramount.  If there's already an existing way to accomplish the same thing in the same size, the feature will be rejected, even if the existing way is difficult to understand.  Redundancy in the language wastes space.
 1. Clarity of the langauge is secondary goal (if you can believe it).  Size is never compromised for clarity, but all else being equal the clear option is chosen.  Clarity is not defined here, but *"I'll know it when I see it."*
 1. All stax programs must be expressable in printable ASCII. (code points 32 to 126)  All ascii stax programs must be able to be represented in Packed stax representation.  I want programs to be editable on a standard keyboard.  Conversion to and form packed will be handled by automated tools.
      * Exception: Non-packed programs can contain non-ASCII characters in string literals and things, and that should work.  However, such programs can never be packed. 
 1. Run-time efficiency of the language is a distant last-place consideration.  Faster is better, but not if it affects clarity or size.
 1. If an existing instruction is found that could have been accomplished equivalently by other means, it will be deprecated.  This has happened a few times.  All instructions that have ever been deprecated still work, but if I run out of instruction space, I will begin re-using some of those.
 1. The language has to be able to run inside a web browser, and cannot access any input outside of its standard input text stream.  No file system, network, http, webcam, audio, or anything else.  Output will be only in terms of text-based standard output.
 1. The input and output are expressed in terms of unicode character streams of unspecified encoding, not bytes.  For command-line invocations interpreter switches can be used to set the character encoding of the input stream if necessary.
