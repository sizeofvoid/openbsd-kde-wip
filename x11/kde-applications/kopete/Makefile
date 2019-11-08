# $OpenBSD: Makefile,v 1.9 2019/03/24 11:56:59 rsadowski Exp $

COMMENT =	multi-protocol instant messenger for KDE
DISTNAME =	kopete-${VERSION}
CATEGORIES =	net x11

SHARED_LIBS +=  kopete                    0.0 # 0.0
SHARED_LIBS +=  kopete_oscar              0.0 # 0.0
SHARED_LIBS +=  kopeteaddaccountwizard    0.0 # 0.0
SHARED_LIBS +=  kopetechatwindow_shared   0.0 # 0.0
SHARED_LIBS +=  kopetecontactlist         0.0 # 0.0
SHARED_LIBS +=  kopeteidentity            0.0 # 0.0
SHARED_LIBS +=  kopeteprivacy             0.0 # 0.0
SHARED_LIBS +=  kopetestatusmenu          0.0 # 0.0
SHARED_LIBS +=  oscar                     0.0 # 0.0
SHARED_LIBS +=  kopete_otr_shared         0.0 # 0.0
SHARED_LIBS +=  qgroupwise                0.0 # 0.0

WANTLIB += ${COMPILER_LIBCXX} KF5Archive KF5Auth KF5Bookmarks
WANTLIB += KF5Codecs KF5Completion KF5ConfigCore KF5ConfigGui
WANTLIB += KF5ConfigWidgets KF5Contacts KF5CoreAddons KF5Crash
WANTLIB += KF5DBusAddons KF5DNSSD KF5Emoticons KF5GuiAddons KF5I18n
WANTLIB += KF5IconThemes KF5IdentityManagement KF5ItemViews KF5JS
WANTLIB += KF5JobWidgets KF5KCMUtils KF5KDELibs4Support KF5KHtml
WANTLIB += KF5KIOCore KF5KIOFileWidgets KF5KIOWidgets KF5Notifications
WANTLIB += KF5NotifyConfig KF5Parts KF5PimTextEdit KF5Service
WANTLIB += KF5Solid KF5SonnetUi KF5TextEditor KF5TextWidgets KF5UnitConversion
WANTLIB += KF5Wallet KF5WidgetsAddons KF5WindowSystem KF5XmlGui
WANTLIB += Qt5Concurrent Qt5Core Qt5DBus Qt5Gui Qt5Network Qt5PrintSupport
WANTLIB += Qt5Sql Qt5Widgets Qt5Xml c gadu idn m otr xml2 xslt
WANTLIB += z

MODULES +=	x11/kde-applications \
		multimedia/phonon

MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes


# XXX
#LIB_DEPENDS devel/jsoncpp not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS net/ortp not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS audio/speex not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS databases/sqlite not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS audio/xmms2 not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS devel/glib2 not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS security/gpgme,-qt not needed for x11/kde-applications/kopete ?
#LIB_DEPENDS x11/kde-applications/libkleo not needed for

LIB_DEPENDS +=	devel/libidn \
		devel/jsoncpp \
		net/libgadu \
		net/ortp \
		security/libotr \
		textproc/libxml \
		textproc/libxslt \
		audio/speex \
		databases/sqlite \
		audio/xmms2 \
		devel/glib2 \
		security/gpgme,-qt

# Not found SRTP security/libsrtp

LIB_DEPENDS +=	devel/kf5/karchive \
		devel/kf5/kauth \
		devel/kf5/kbookmarks \
		devel/kf5/kcmutils \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcrash \
		devel/kf5/kdbusaddons \
		devel/kf5/kdelibs4support \
		devel/kf5/kdnssd \
		devel/kf5/kemoticons \
		devel/kf5/kguiaddons \
		devel/kf5/khtml \
		devel/kf5/ki18n \
		devel/kf5/kiconthemes \
		devel/kf5/kio \
		devel/kf5/kitemviews \
		devel/kf5/kjobwidgets \
		devel/kf5/kjs \
		devel/kf5/knotifications \
		devel/kf5/knotifyconfig \
		devel/kf5/kparts \
		devel/kf5/kservice \
		devel/kf5/ktexteditor \
		devel/kf5/ktextwidgets \
		devel/kf5/kunitconversion \
		devel/kf5/kwallet \
		devel/kf5/kwidgetsaddons \
		devel/kf5/kwindowsystem \
		devel/kf5/kxmlgui \
		devel/kf5/solid \
		devel/kf5/sonnet \
		x11/kde-applications/kcontacts \
		x11/kde-applications/kidentitymanagement \
		x11/kde-applications/libkleo

#TEST_IS_INTERACTIVE =	X11
PORTHOME =		${WRKDIR}

CONFIGURE_ARGS +=	-DDISABLE_VIDEOSUPPORT=ON \
			-DMOZPLUGIN_INSTALL_DIR=${LOCALBASE}/lib/mozilla/plugins

# Kopete meanwhile code is broken
CONFIGURE_ARGS +=	-DCMAKE_DISABLE_FIND_PACKAGE_LibMeanwhile=ON

CONFIGURE_ARGS +=	-DCMAKE_C_FLAGS="${CFLAGS} -I${LOCALBASE}/include" \
			-DCMAKE_CXX_FLAGS="${CXXFLAGS} -I${LOCALBASE}/include" \
			-DCMAKE_EXE_LINKER_FLAGS="${LDFLAGS} -L${X11BASE}/lib -L${LOCALBASE}/lib"

post-patch:
	cd ${WRKSRC}; perl -pi -e 's/X11_Xss_/X11_Xscreensaver_/g' \
		CMakeLists.txt \
		libkopete/CMakeLists.txt

.include <bsd.port.mk>
