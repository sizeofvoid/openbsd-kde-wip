# openbsd-kde-wip work in progress KDE ports

## Finished but not yet imported to CVS

All these ports require reviews and tests.

- development
    - :ok: [akonadi](x11/kde-applications/akonadi)
    - :ok: [akonadi-mime](x11/kde-applications/akonadi-mime)
    - :ok: [grantleetheme](x11/kde-applications/grantleetheme)
    - :ok: [kcontacts](x11/kde-applications/kcontacts)
- education
    - :ok: [kwordquiz](x11/kde-applications/kwordquiz)
    - :ok: [minuet](x11/kde-applications/minuet)
    - :ok: [rocs](x11/kde-applications/rocs)
- games
    - :no_entry: [knights](x11/kde-applications/knights)
       -  runtime issue: Can't find chess engine, QIODevice::write (KProcess): device not open
    - :ok: [picmi](x11/kde-applications/picmi)
- graphics
    - :ok: [kamera](x11/kde-applications/kamera)
    - :ok: [kcolorchooser](x11/kde-applications/kcolorchooser)
    - :ok: [kdegraphics-thumbnailers](x11/kde-applications/kdegraphics-thumbnailers)
    - :ok: [kolourpaint](x11/kde-applications/kolourpaint)
    - :ok: [kruler](x11/kde-applications/kruler)
- internet / network
    - :ok: [kdenetwork-filesharing](x11/kde-applications/kdenetwork-filesharing)
    - :no_entry: [kget](x11/kde-applications/kget)
       -  runtime issue: crazy runtime behavior. Sometimes it's stuck, floating point exception
    - :ok: [picmi](x11/kde-applications/picmi)
- multimedia
    - :ok: [juk](x11/kde-applications/juk)
- utilities
    - :ok: [kwalletmanager](x11/kde-applications/kwalletmanager)
    - :ok: [sweeper](x11/kde-applications/sweeper)

## How to use this tree

One way to use this tree is to clone it into your `/usr/ports/mystuff`
directory and adjust `PORTSDIR_PATH` accordingly in /etc/mk.conf:

	PORTSDIR_PATH=${PORTSDIR}/mystuff/openbsd-kde-wip:${PORTSDIR}

In the above example, a port with version 1 in `/usr/ports/mystuff/openbsd-kde-wip`,
version 2 in cvs.  Then, the version in openbsd-kde-wip will be picked up before
the version in cvs.

## How can you help!?

Checkout the repository and simply build and test your software of choice from
the list above. **Feedback is very important to me**. If the port work, tell me.
If it's broken or other notable issues show up, tell me.

The best way is via e-mail: <rsadowski@openbsd.org>
