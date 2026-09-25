COMMENT =	remote-controlled bipedal tanks 3D networked action FPS

V =		0.7.1
GH_ACCOUNT =	avaraline
GH_PROJECT =	Avara
GH_TAGNAME =	${V}
PKGNAME=avara-${V}

#
# On source code hosting platforms use static tarballs over generated ones.
# It's easy to distinguish between them on github, gitlab and codeberg by
# looking at the file URL:
# /releases/ -> preferred. Use SITES and DISTNAME.
# /archive/ -> use DIST_TUPLE (use only if there is no release version).
#
# platform: codeberg, github, gitlab, kde, srht, gnome, fdo
# account: usually the account or organisation name
# project: the project or repository name
# id: either a tag name or commit hash.
#   Tag names with standard tag formats, like 1.0.1 or v1.0, set an
#   appropriate PKGNAME automatically. Otherwise, set it yourself.
#   "make show=PKGNAMES" will help identify if that's needed.
#   For a commit hash, use the full hash (not shortened), and set PKGNAME.
# subdir: usually ".", otherwise the extracted files are moved to another
#   directory under WRKDIST. Mostly useful for git submodules.
#DIST_TUPLE +=	platform account project id subdir

# the category used in the directory name, /usr/ports/<category>/portname,
# must be included and listed first.
CATEGORIES =	games

HOMEPAGE =	https://github.com/avaraline/Avara

MAINTAINER =	Morgan Aldridge <morgant@makkintosshu.com>

# MIT, zlib, BSD 3-clause, Happy Bunny (MIT), Boost Software
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} GL GLU SDL2 c m

#SITES =		???

# C++17
COMPILER =		base-clang ports-gcc

# Dependencies
BUILD_DEPENDS =		net/rsync
LIB_DEPENDS =		devel/sdl2 audio/sdl2-audiolib devel/sdl2-net
#TEST_DEPENDS =		???

MAKE_FLAGS =		CC=${CC} CXX=${CXX} GIT_HASH=${V} GIT_BRANCH=OpenBSD
MAKE_ENV =		CPPFLAGS=-I${LOCALBASE}/include \
			LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib \
			-L${X11BASE}/lib"
#FAKE_FLAGS =		???
#TEST_FLAGS =		???

USE_GMAKE =		Yes
CONFIGURE_STYLE =	none

# if debug packages are a good idea, extra configure args may be necessary
# and DEBUG_PACKAGES will commonly be set to ${BUILD_PACKAGES}
#DEBUG_CONFIGURE_ARGS =	???
#DEBUG_PACKAGES = ${BUILD_PACKAGES}

#NO_TEST =		Yes

# Overrides for default values
#
#CFLAGS +=		-I${LOCALBASE}/include -I${X11BASE}/include
#CXXFLAGS +=		-I${LOCALBASE}/include -I${X11BASE}/include
#LDFLAGS =		???

ALL_TARGET =		avara
#INSTALL_TARGET =	???
#TEST_TARGET =		???

post-install:
	${INSTALL_SCRIPT} ${FILESDIR}/avara.sh ${PREFIX}/bin/avara

.include <bsd.port.mk>
