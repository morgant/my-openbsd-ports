# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

V =		0.113
COMMENT =	FUSE driver for HFS+ filesystems
DISTNAME =	hfsfuse-${V}
CATEGORIES =	sysutils

HOMEPAGE =	https://github.com/0x09/hfsfuse
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB =	c fuse pthread utf8proc

MASTER_SITES =	https://github.com/0x09/hfsfuse/releases/download/$V/

LIB_DEPENDS =	www/netsurf/libutf8proc

USE_GMAKE =		Yes
CONFIGURE_STYLE =	simple
CONFIGURE_SCRIPT =	/usr/local/bin/gmake
CONFIGURE_ARGS =	config WITH_UBLIO=none WITH_UTF8PROC=system
NO_TEST =		Yes

pre-install:
	sed -i "s@PREFIX=${TRUEPREFIX}@@g" ${WRKSRC}/config.mak

.include <bsd.port.mk>
