# $OpenBSD: Makefile.template,v 1.79 2019/03/03 23:18:37 sthen Exp $
#
# Use /usr/ports/infrastructure/bin/portcheck

COMMENT =	version Control System for HOME

VERSION =	1.20151229
DISTNAME =	v$(VERSION)
PKGNAME =	vcsh-$(VERSION)

GH_ACCOUNT =	RichiH
GH_PROJECT =	vcsh
GH_TAGNAME =	$(DISTNAME)

CATEGORIES =	devel

HOMEPAGE =	https://github.com/RichiH/vcsh

# GPLv2
PERMIT_PACKAGE_CDROM= Yes

BUILD_DEPENDS =		devel/p5-Test-Most \
			devel/p5-Shell-Command
RUN_DEPENDS =		devel/git

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/vcsh ${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/vcsh.1 ${PREFIX}/man/man1
	mkdir -p ${PREFIX}/share/vcsh
	${INSTALL_DATA} ${WRKSRC}/README.md ${PREFIX}/share/vcsh
	${INSTALL_DATA} ${WRKSRC}/doc/hooks ${PREFIX}/share/vcsh
	mkdir -p ${WRKSRC}/share/zsh/vendor-completions
	${INSTALL_DATA} ${WRKSRC}/_vcsh ${PREFIX}/share/zsh/vendor-completions

.include <bsd.port.mk>
