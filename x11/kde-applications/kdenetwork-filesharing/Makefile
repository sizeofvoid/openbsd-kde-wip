# $OpenBSD: Makefile,v 1.1.1.1 2018/07/28 18:52:19 rsadowski Exp $

COMMENT =	KDE Filesharing via Samba
DISTNAME =	kdenetwork-filesharing-${VERSION}
CATEGORIES =	net devel

WANTLIB += ${COMPILER_LIBCXX} KF5Completion KF5ConfigCore KF5CoreAddons
WANTLIB += KF5I18n KF5JobWidgets KF5KIOCore KF5KIOWidgets KF5Service
WANTLIB += KF5WidgetsAddons Qt5Concurrent Qt5Core Qt5DBus Qt5Gui
WANTLIB += Qt5Network Qt5Widgets m

MODKDE5_TRANSLATIONS = yes

MODULES +=	x11/kde-applications

BUILD_DEPENDS =	devel/kf5/kitemviews \
		devel/kf5/solid \
		devel/kf5/kauth \
		devel/kf5/kcodecs \
		devel/kf5/kconfigwidgets

LIB_DEPENDS =	devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/ki18n \
		devel/kf5/kio \
		devel/kf5/kjobwidgets \
		devel/kf5/kwidgetsaddons \
		devel/kf5/kservice \
		devel/kf5/kcoreaddons

.include <bsd.port.mk>
