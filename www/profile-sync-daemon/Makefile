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

RUN_DEPENDS =		shells/bash net/rsync x11/xdg-user-dirs-gtk x11/dbus

USE_GMAKE =		Yes
CONFIGURE_STYLE =	none
NO_BUILD =		Yes

FAKE_FLAGS =		DESTDIR=

NO_TEST =		Yes

pre-configure:
	sed -i "s,/bin/bash,/usr/bin/env bash," \
		${WRKSRC}/common/profile-sync-daemon.in \
		${WRKSRC}/common/psd-suspend-sync
	sed -Ei "s/(PSNAME=\")[^\"]+/\1chrome/" \
		${WRKSRC}/common/browsers/chromium
	rm ${WRKSRC}/common/browsers/chromium-dev

post-install:
	sed -i "s,${PREFIX}/share/psd,${TRUEPREFIX}/share/psd," ${PREFIX}/bin/profile-sync-daemon

.include <bsd.port.mk>
