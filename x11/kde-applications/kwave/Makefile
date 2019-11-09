# $OpenBSD: Makefile,v 1.4 2019/03/24 11:56:58 rsadowski Exp $

COMMENT =	audio file editor
DISTNAME =	kwave-${VERSION}
CATEGORIES =	audio

HOMEPAGE =	https://kde.org/applications/multimedia/org.kde.kwave


MODKDE5_TRANSLATIONS = yes
MODKDE5_DOCS = yes

MODULES +=	x11/kde-applications

LIB_DEPENDS +=	audio/libsamplerate \
		audio/id3lib \
		audio/libvorbis

LIB_DEPENDS +=	\
		devel/kf5/attica \
		devel/kf5/baloo \
		devel/kf5/bluez-qt \
		devel/kf5/breeze-icons \
		devel/kf5/extra-cmake-modules \
		devel/kf5/frameworkintegration \
		devel/kf5/kactivities \
		devel/kf5/kactivities-stats \
		devel/kf5/kapidox \
		devel/kf5/karchive \
		devel/kf5/kauth \
		devel/kf5/kbookmarks \
		devel/kf5/kcmutils \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcoreaddons \
		devel/kf5/kcrash \
		devel/kf5/kdbusaddons \
		devel/kf5/kdeclarative \
		devel/kf5/kded \
		devel/kf5/kdelibs4support \
		devel/kf5/kdesignerplugin \
		devel/kf5/kdesu \
		devel/kf5/kdewebkit \
		devel/kf5/kdnssd \
		devel/kf5/kdoctools \
		devel/kf5/kemoticons \
		devel/kf5/kfilemetadata \
		devel/kf5/kglobalaccel \
		devel/kf5/kguiaddons \
		devel/kf5/kholidays \
		devel/kf5/khtml \
		devel/kf5/ki18n \
		devel/kf5/kiconthemes \
		devel/kf5/kidletime \
		devel/kf5/kimageformats \
		devel/kf5/kinit \
		devel/kf5/kio \
		devel/kf5/kirigami2 \
		devel/kf5/kitemmodels \
		devel/kf5/kitemviews \
		devel/kf5/kjobwidgets \
		devel/kf5/kjs \
		devel/kf5/kjsembed \
		devel/kf5/kmediaplayer \
		devel/kf5/knewstuff \
		devel/kf5/knotifications \
		devel/kf5/knotifyconfig \
		devel/kf5/kpackage \
		devel/kf5/kparts \
		devel/kf5/kpeople \
		devel/kf5/kplotting \
		devel/kf5/kpty \
		devel/kf5/kross \
		devel/kf5/krunner \
		devel/kf5/kservice \
		devel/kf5/ktexteditor \
		devel/kf5/ktextwidgets \
		devel/kf5/kunitconversion \
		devel/kf5/kwallet \
		devel/kf5/kwidgetsaddons \
		devel/kf5/kwindowsystem \
		devel/kf5/kxmlgui \
		devel/kf5/kxmlrpcclient \
		devel/kf5/oxygen-icons \
		devel/kf5/plasma-framework \
		devel/kf5/prison \
		devel/kf5/purpose \
		devel/kf5/qqc2-desktop-style \
		devel/kf5/solid \
		devel/kf5/sonnet \
		devel/kf5/syntax-highlighting \
		devel/kf5/threadweaver

CONFIGURE_ARGS +=	-DWITH_OSS=OFF \
			-DWITH_ALSA=OFF \
			-DWITH_MP3=OFF

CONFIGURE_ARGS +=	-DCMAKE_C_FLAGS="${CFLAGS} -I${LOCALBASE}/include" \
			-DCMAKE_CXX_FLAGS="${CXXFLAGS} -I${LOCALBASE}/include" \
			-DCMAKE_EXE_LINKER_FLAGS="${LDFLAGS} -L${X11BASE}/lib -L${LOCALBASE}/lib"

.include <bsd.port.mk>
