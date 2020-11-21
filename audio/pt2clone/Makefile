# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $
#

ONLY_FOR_ARCHS =	amd64
COMMENT =		portable ProTracker 2 (v2.3D) clone
PKGNAME =		pt2clone-1.25
CATEGORIES =		audio x11

GH_ACCOUNT =	8bitbubsy
GH_PROJECT =	pt2-clone
GH_TAGNAME =	v1.25_fix

HOMEPAGE =	https://16-bits.org/pt2.php
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# BSD
PERMIT_PACKAGE =	Yes

WANTLIB +=		c m SDL2

LIB_DEPENDS =		devel/sdl2

CONFIGURE_STYLE =	none

NO_TEST =		Yes

CFLAGS +=		-I/usr/local/include \
			-L/usr/local/lib \
			-lSDL2 \
			-lm

.include <bsd.port.mk>
