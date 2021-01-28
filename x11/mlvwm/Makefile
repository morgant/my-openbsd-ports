# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	Macintosh-like virtual window manager

V =		0.9.2
DISTNAME =	mlvwm-$V
CATEGORIES =	x11

HOMEPAGE =	https://github.com/morgant/mlvwm/
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# part MIT part Freeware, see README.md
PERMIT_PACKAGE =	Yes

WANTLIB +=		X11 Xau Xdmcp Xext Xpm c

MASTER_SITES =		https://github.com/morgant/mlvwm/releases/download/$V/

CONFIGURE_STYLE =	imake
MAKE_FLAGS =		CC="${CC}" COPTS="${CFLAGS}"
NO_TEST =		Yes

.include <bsd.port.mk>
