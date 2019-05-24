# $OpenBSD: Makefile.template,v 1.79 2019/03/03 23:18:37 sthen Exp $

COMMENT =	Snappy terminal file manager for the ninjas

VERSION =	2.4
DISTNAME =	nnn-v$(VERSION)
PKGNAME =	nnn-$(VERSION)

GH_ACCOUNT =	jarun
GH_PROJECT =	nnn
GH_TAGNAME =	v$(VERSION)

CATEGORIES =	misc

HOMEPAGE =	https://github.com/jarun/nnn

# BSD2
PERMIT_PACKAGE_CDROM= Yes

# build/configuration variables
USE_GMAKE =		Yes

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/nnn ${PREFIX}/bin
	$(INSTALL_MAN) ${WRKSRC}/nnn.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
