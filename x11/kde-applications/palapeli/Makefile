# $OpenBSD: Makefile,v 1.3 2019/03/24 11:57:04 rsadowski Exp $

COMMENT =	jigsaw puzzle game
DISTNAME =	palapeli-${VERSION}
CATEGORIES =	games
REVISION =	0

HOMEPAGE =	https://www.kde.org/applications/games/palapeli


SHARED_LIBS +=  pala                      0.0 # 0.2

WANTLIB += ${COMPILER_LIBCXX} KF5Archive KF5Auth KF5Codecs KF5Completion
WANTLIB += KF5ConfigCore KF5ConfigGui KF5ConfigWidgets KF5CoreAddons
WANTLIB += KF5Crash KF5I18n KF5ItemViews KF5JobWidgets KF5KIOCore
WANTLIB += KF5KIOWidgets KF5Notifications KF5Service KF5WidgetsAddons
WANTLIB += KF5XmlGui Qt5Concurrent Qt5Core Qt5DBus Qt5Gui Qt5Network
WANTLIB += Qt5Svg Qt5Widgets Qt5Xml c m

MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes

MODULES +=	x11/kde-applications

BUILD_DEPENDS +=x11/kde-applications/libkdegames
RUN_DEPENDS +=	misc/shared-mime-info

LIB_DEPENDS +=	devel/kf5/karchive \
		devel/kf5/kauth \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcoreaddons \
		devel/kf5/kcrash \
		devel/kf5/ki18n \
		devel/kf5/kio  \
		devel/kf5/kitemviews  \
		devel/kf5/knotifications  \
		devel/kf5/kservice  \
		devel/kf5/kwidgetsaddons \
		devel/kf5/kxmlgui \
		x11/qt5/qtsvg

.include <bsd.port.mk>
