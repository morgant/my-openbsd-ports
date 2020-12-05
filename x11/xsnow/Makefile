# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	let it snow on the root, in between, and on X11 windows
DISTNAME =	xsnow-1.42
CATEGORIES =	x11

HOMEPAGE =	https://janswaal.home.xs4all.nl/Xsnow/

MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# Freeware
PERMIT_PACKAGE =	Yes

WANTLIB +=		X11 Xau Xdmcp Xext Xpm c m
MASTER_SITES =		https://janswaal.home.xs4all.nl/Xsnow/

BUILD_DEPENDS =		devel/imake
CONFIGURE_STYLE =	imake
NO_TEST =		Yes

.include <bsd.port.mk>
