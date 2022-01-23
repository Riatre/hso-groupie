## hso groupie

### What

hso groupie is a pwnable challenge in Real World CTF 4th. The challenge asks
players to write an exploit for the pdftohtml utility in Xpdf 4.03, running on
Debian unstable. The intended bug is the one documented in
[A deep dive into an NSO zero-click iMessage exploit: Remote Code Execution](https://googleprojectzero.blogspot.com/2021/12/a-deep-dive-into-nso-zero-click.html).

The bug is also not fixed in [Poppler](https://gitlab.freedesktop.org/poppler/poppler) as of Jan 23.
I picked the original Xpdf for this challenge due to a few 
[funny sanity checks](https://fossies.org/diffs/xpdf/4.02_vs_4.03/xpdf/JBIG2Stream.cc-diff.html),
which could be trivially bypassed, might give extra lulz.

Team 'NeSE' solved it within the first 90 minutes of the game, likely due to
they already have an exploit ready for this target.  In hindsight due to the
bug being quite popular the challenge probably just shouldn't happen.

### Is there a writeup?

No. I don't have time for a full writeup.

The exploit really just does what [this blog post](https://googleprojectzero.blogspot.com/2021/12/a-deep-dive-into-nso-zero-click.html)
said, except the "build a computer" part, as there is no need to search memory
or do complicated exploit engineering due to the nature of the challenge (on
Linux, only needs a PoC exploit instead of a *weaponized* one). A few
full-adders is enough for computing address at fixed offset and run
`system("whatever")`.

The exploit code is also (hopefully) reasonably readable, so you may just read
that.
