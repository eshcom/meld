--install:
sudo python3 setup.py install --prefix=/usr


--for test:
meld /usr/share/gtksourceview-2.0/language-specs/cpp.lang /usr/share/gtksourceview-3.0/language-specs/cpp.lang
