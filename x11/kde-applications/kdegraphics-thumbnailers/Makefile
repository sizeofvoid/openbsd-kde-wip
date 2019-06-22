# $OpenBSD: Makefile,v 1.1.1.1 2018/07/28 18:52:19 rsadowski Exp $

COMMENT =	thumbnailers for various graphics file formats
DISTNAME =	kdegraphics-thumbnailers-${VERSION}
CATEGORIES =	devel graphics

KDE5 =		Yes

WANTLIB += ${COMPILER_LIBCXX} KF5Completion KF5ConfigCore KF5CoreAddons
WANTLIB += KF5JobWidgets KF5KDcraw KF5KExiv2 KF5KIOCore KF5KIOWidgets
WANTLIB += KF5Service KF5WidgetsAddons Qt5Concurrent Qt5Core Qt5DBus
WANTLIB += Qt5Gui Qt5Network Qt5Widgets m

MODULES +=	x11/kde-applications

LIB_DEPENDS +=	devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kio \
		devel/kf5/kjobwidgets \
		devel/kf5/kservice \
		devel/kf5/kwidgetsaddons \
		x11/kde-applications/libkexiv2 \
		x11/kde-applications/libkdcraw

NO_TEST =	Yes

.include <bsd.port.mk>