COMMENT =	implementation of the NewtonScript prototype-based language

V =		20221021
DISTNAME =	newt64-0.0.${V}
CATEGORIES =	lang

GH_ACCOUNT =	MatthiasWM
GH_PROJECT =	NEWT64
GH_COMMIT =	de7fab00cb4f616aa73457d8b3ba7975035eff8c

HOMEPAGE =	https://github.com/MatthiasWM/NEWT64
MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# GPLv2, MIT (install-sh), MPL 1.1 (contrib/{NewtObjC,NativeCalls}/*)
PERMIT_PACKAGE =	Yes

MODULES	=	devel/cmake

WANTLIB += 	c

BUILD_DEPENDS =	devel/bison

pre-configure:
	sed -i "s/2020\.4\.5/${V}/" ${WRKSRC}/CMakeLists.txt

.include <bsd.port.mk>
