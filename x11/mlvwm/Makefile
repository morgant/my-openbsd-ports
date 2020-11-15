# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	Macintosh-like virtual window manager
DISTNAME =	mlvwm091
PKGNAME =	mlvwm-0.91
CATEGORIES =	x11

HOMEPAGE =	http://www2u.biglobe.ne.jp/~y-miyata/mlvwm.html
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# Freeware
PERMIT_PACKAGE =	Yes

WANTLIB =		X11 Xau Xdmcp Xext Xpm c
MASTER_SITES =		http://www2u.biglobe.ne.jp/~y-miyata/mlvwm/

BUILD_DEPENDS =		devel/imake
CONFIGURE_STYLE =	imake
NO_TEST =		Yes

.include <bsd.port.mk>
