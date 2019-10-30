# $OpenBSD: Makefile,v 1.6 2019/06/19 19:45:59 kili Exp $

COMMENT =	dock based on Plasma Frameworks
VERSION =	0.9.4
DISTNAME =	latte-dock-${VERSION}
CATEGORIES =	textproc

MASTER_SITES =	https://download.kde.org/stable/latte-dock/


MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes

MODULES +=	x11/kde-applications \
		multimedia/phonon


TEST_IS_INTERACTIVE =	X11

.include <bsd.port.mk>
