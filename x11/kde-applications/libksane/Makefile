# $OpenBSD: Makefile,v 1.4 2019/03/24 11:57:04 rsadowski Exp $

COMMENT =	KDE SANE (scanner) wrapper library
DISTNAME =	libksane-${VERSION}
PKGNAME =	libksane-kf5-${VERSION}
CATEGORIES =	graphics devel
REVISION =	0


SHARED_LIBS +=  KF5Sane                   0.0 # 5.1

WANTLIB += ${COMPILER_LIBCXX} KF5I18n KF5SonnetUi KF5TextWidgets
WANTLIB += KF5Wallet KF5WidgetsAddons Qt5Core Qt5Gui Qt5Widgets
WANTLIB += m sane

MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes

MODULES +=	x11/kde-applications

LIB_DEPENDS +=	devel/kf5/ki18n \
		devel/kf5/ktextwidgets \
		devel/kf5/kwallet \
		devel/kf5/kwidgetsaddons \
		devel/kf5/sonnet \
		graphics/sane-backends

.include <bsd.port.mk>
