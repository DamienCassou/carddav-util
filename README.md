carddav-copy
============

*carddav-copy* is a python scripts that moves contact information between
a CardDAV server and a local file. It can dump entire addressbook to
a vCard file and then re-upload this information to another CardDAV
server.

Requirements
------------

The following python libraries are required:

 * requests
 * vobject
 * lxml

On ubuntu:

    sudo apt-get install python-requests python-vobject python-lxml

Usage
-----

ownCloud:

    ./carddav-copy.py   \
        --download      \
        --user=username \
        --file=test.vcf \
        --url=https://domain.com/owncloud/remote.php/carddav/addressbooks/username/contacts

Baïkal:

    ./carddav-copy.py   \
        --download      \
        --user=username \
        --file=test.vcf \
        --url=https://domain.com/baikal/card.php/addressbooks/username/bookid

Where:
 * username is youre username - the one that you specified on the commandline
 * bookid is the identifier of your addressbook

Authentication:
 * If your server uses digest authentication, you need to add *--digest*.

License
-------

Copyright (c) 2012, Lukasz Janyst &lt;ljanyst@buggybrain.net&gt;

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED 'AS IS' AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
