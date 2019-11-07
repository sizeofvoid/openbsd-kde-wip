# openbsd-kde-wip work in progress KDE ports

## Finished but not yet imported to CVS

All these ports require reviews and tests.

- development
    - :ok: [akonadi](x11/kde-applications/akonadi)
    - :ok: [akonadi-mime](x11/kde-applications/akonadi-mime)
    - :ok: [kcontacts](x11/kde-applications/kcontacts)
- games
    - :no_entry: [knights](x11/kde-applications/knights)
       -  runtime issue: Can't find chess engine, QIODevice::write (KProcess): device not open
- graphics
    - :ok: [kdegraphics-thumbnailers](x11/kde-applications/kdegraphics-thumbnailers)
- internet / network
    - :ok: [kdenetwork-filesharing](x11/kde-applications/kdenetwork-filesharing)
    - :no_entry: [kget](x11/kde-applications/kget)
       -  runtime issue: crazy runtime behavior. Sometimes it's stuck, floating point exception
    - :ok: [krdc](x11/kde-applications/krdc)
    - :ok: [krfb](x11/kde-applications/krfb)
- multimedia
    - :ok: [kmix](x11/kde-applications/kmix)
- utilities
    - :ok: [kcharselect](x11/kde-applications/kcharselect)
    - :ok: [kdebugsettings](x11/kde-applications/kdebugsettings)
    - :ok: [kbackup](x11/kde-applications/kbackup)
    - :ok: [kteatime](x11/kde-applications/kteatime)
    - :ok: [ktimer](x11/kde-applications/ktimer)

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
