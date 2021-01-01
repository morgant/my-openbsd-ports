# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	Macintosh-like virtual window manager
DISTNAME =	mlvwm-0.9.2
CATEGORIES =	x11

HOMEPAGE =	https://github.com/morgant/mlvwm/
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# Freeware
PERMIT_PACKAGE =	Yes

WANTLIB +=		X11 Xau Xdmcp Xext Xpm c
MASTER_SITES =		https://github.com/morgant/mlvwm/releases/download/0.9.2/

BUILD_DEPENDS =		devel/imake
CONFIGURE_STYLE =	imake
NO_TEST =		Yes

.include <bsd.port.mk>
