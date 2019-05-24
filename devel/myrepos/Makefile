# $OpenBSD: Makefile.template,v 1.79 2019/03/03 23:18:37 sthen Exp $

COMMENT =	Tool to manage all your version control repos

VERSION =	2018032701
DISTNAME =	$(VERSION)
PKGNAME =	myrepos-$(VERSION)

GH_ACCOUNT =	towo
GH_PROJECT =	myrepos
GH_TAGNAME =	$(DISTNAME)

CATEGORIES =	devel

HOMEPAGE =	https://github.com/towo/myrepos

# GPLv2
PERMIT_PACKAGE_CDROM= Yes

NO_BUILD =	Yes

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/mr ${PREFIX}/bin
	${INSTALL_PROGRAM} ${WRKSRC}/webcheckout ${PREFIX}/bin
	@pod2man -c ${WRKSRC}/mr ${WRKSRC}/mr > ${WRKSRC}/mr.1
	@(cd ${WRKSRC}; pod2man -c webcheckout webcheckout > webcheckout.1)
	${INSTALL_MAN} ${WRKSRC}/mr.1 ${PREFIX}/man/man1
	${INSTALL_MAN} ${WRKSRC}/webcheckout.1 ${PREFIX}/man/man1
	@mkdir -p ${PREFIX}/share/mr
	${INSTALL_DATA} ${WRKSRC}/lib/* ${PREFIX}/share/mr

.include <bsd.port.mk>
