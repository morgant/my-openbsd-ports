COMMENT =	symlinks and syncs browser profile dirs to RAM

V =		6.48
DISTNAME =	profile-sync-daemon-$V
CATEGORIES =	www

GH_ACCOUNT =	graysky2
GH_PROJECT =	profile-sync-daemon
GH_TAGNAME =	v$V

HOMEPAGE =	https://github.com/graysky2/profile-sync-daemon/
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# MIT
PERMIT_PACKAGE =	Yes

# "make port-lib-depends-check" can help
#WANTLIB =		???

# Fix dos line-endings in files needing patches
#FIX_CRLF_FILES =	???

# Optional subdirectory of DISTDIR where distfiles and patches will be placed
#DIST_SUBDIR =		???

# Dependencies
BUILD_DEPENDS =		net/rsync
RUN_DEPENDS =		shells/bash net/rsync x11/xdg-user-dirs-gtk x11/dbus
#LIB_DEPENDS =		???
#TEST_DEPENDS =		???

#MAKE_FLAGS =		???
#MAKE_ENV =		???
FAKE_FLAGS =		DESTDIR=
#TEST_FLAGS =		???

# build/configuration variables
#
USE_GMAKE =		Yes
CONFIGURE_STYLE =	none
NO_BUILD =		Yes
NO_TEST =		Yes

# Assume you have one multiple choice flavor: 1 2 3 and switches a b.
# You would write
#
#FLAVORS =	1 2 3 a b
#FLAVOR ?=
# grab multiple choice value
#CHOICE = ${FLAVOR:Na:Nb}
# check that CHOICE is 1 OR 2 OR 3, or error out
#.if ${CHOICE} == "1"
# code for 1
#.elif ${CHOICE} == "2"
# code for 2
#.elif ${CHOICE} == "3"
# code for 3
#.else
#ERRORS += "Fatal: Conflicting flavor: ${FLAVOR}"
#.endif
# check for switches
#.if ${FLAVOR:Ma}
# code for a
#.endif
#.if ${FLAVOR:Mb}
# code for b
#.endif

# Overrides for default values
#
#CFLAGS =		???
#LDFLAGS =		???
#MAKE_FILE =		???
#PKG_ARCH =		??? (* for arch-independent packages)
#WRKDIST =		??? if other than ${WRKDIR}/${DISTNAME}
#WRKSRC =		??? if other than ${WRKDIST}
#WRKBUILD =		??? if other than ${WRKSRC}
#WRKCONF =		??? if other than ${WRKBUILD}

#ALL_TARGET =		???
#INSTALL_TARGET =	???
#TEST_TARGET =		???

pre-configure:
	sed -i "s,/bin/bash,/usr/bin/env bash," \
		${WRKSRC}/common/profile-sync-daemon.in \
		${WRKSRC}/common/psd-suspend-sync
	sed -Ei "s/(PSNAME=\")[^\"]+/\1chrome/" \
		${WRKSRC}/common/browsers/chromium
	rm ${WRKSRC}/common/browsers/chromium-dev

.include <bsd.port.mk>
