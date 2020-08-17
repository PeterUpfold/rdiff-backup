
`tools/setup-testfiles.sh`

There seems to be an issue extracting this file with the built-in BSD tar and GNU tar -- not sure if it is important:
`x rdiff-backup_testfiles/corrupt_dest1/ث?Wb??]\212?\025v*?\017!?>?Y\206???p?\204\023k\035???e?U\202\232UV???4??X\003\202\as?\236\213?4\004\237\027 ?\217??\227?ج?\205?KvC?#\224\222\236ɷ?_\017\204g\232B\021<=^?M\023\226c\213?|*"\\'^$@#!(){}?+ ~`` : Can't create 'rdiff-backup_testfiles/corrupt_dest1/ث?Wb??]\212?\025v*?\017!?>?Y\206???p?\204\023k\035???e?U\202\232UV???4??X\003\202\as?\236\213?4\004\237\027 ?\217??\227?ج?\205?KvC?#\224\222\236ɷ?_\017\204g\232B\021<=^?M\023\226c\213?|*"\\'^$@#!(){}?+ ~`` '`


`mkdir testfiles`

Install all the Pythons to be able to run the test suite, as well as librsync. Maybe Homebrew is possible too, but I'm using MacPorts here.

`sudo port install python35 python36 python37 python38 librsync`

`pip3 install tox`

`export LIBRSYNC_DIR=/opt/local`
`python3 -m tox -c tox_mac.ini`