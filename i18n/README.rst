Translations
------------
This is how to generate the po template file from top level repository directory::

    # extract strings from ui files
    intltool-extract --type=gettext/glade ui/config.glade
    intltool-extract --type=gettext/glade ui/choose.glade

    # generate subliminal.pot
    xgettext -k_ -kN_ -w 120 --from-code=utf-8 -o i18n/subliminal.pot ui/config.glade.h ui/choose.glade.h nautilus-subliminal.py

    # clean up
    rm ui/*.h

.. _Subliminal: https://github.com/Diaoul/subliminal
