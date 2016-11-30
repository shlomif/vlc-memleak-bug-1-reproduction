This reproduces a problem in VLC that appears to be a memory leak.

Run `sh down.sh` to download the files from YouTube - you'll need
[youtube-dl](http://rg3.github.io/youtube-dl/) .

Run `sh run-vlc.sh` to start VLC.

Run `perl stress-vlc.pl` to swich videos rapidly and cause the leak. You'll
need Perl 5 and https://metacpan.org/release/Net-Telnet . Observe its memory
use in top or htop.

Also see [this bug report](https://github.com/i-rinat/libvdpau-va-gl/issues/63)

Tested on Mageia Linux x86-64 v6 with [these specs](http://www.shlomifish.org/meta/FAQ/#computers-specs) .
