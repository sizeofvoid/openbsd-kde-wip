# $OpenBSD: Makefile,v 1.5 2019/03/24 11:56:59 rsadowski Exp $

COMMENT =	Sokoban-like logic game
DISTNAME =	kpat-${VERSION}
CATEGORIES =	games



MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes

MODULES +=	x11/kde-applications

BUILD_DEPENDS +=x11/qt5/qtquickcontrols
RUN_DEPENDS +=	x11/qt5/qtquickcontrols

LIB_DEPENDS +=	devel/kf5/kauth \
		devel/kf5/kcodecs \
		devel/kf5/ki18n \
		devel/kf5/kcrash \
		devel/kf5/kdbusaddons \
		devel/kf5/kconfig \
		devel/kf5/kcoreaddons \
		devel/kf5/kwidgetsaddons \
		devel/kf5/knewstuff \
		devel/kf5/kxmlgui \
		x11/qt5/qtdeclarative \
		x11/kde-applications/libkdegames

.include <bsd.port.mk>
