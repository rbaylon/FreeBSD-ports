PORTNAME=	z
PORTVERSION=	1.12
DISTVERSIONPREFIX=	v
CATEGORIES=	sysutils

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Takes you to your most used directories, based on "frecency"
WWW=		https://github.com/rupa/z/

LICENSE=	WTFPL

USE_GITHUB=	yes
GH_ACCOUNT=	rupa

NO_BUILD=	yes
NO_ARCH=	yes
SUB_FILES=	pkg-message
PLIST_FILES=	${DATADIR_REL}/z.sh \
		man/man1/z.1.gz

do-install:
	${MKDIR} ${STAGEDIR}${DATADIR}
	${INSTALL_SCRIPT} ${WRKSRC}/z.sh ${STAGEDIR}${DATADIR}
	${INSTALL_MAN} ${WRKSRC}/z.1 ${STAGEDIR}${MAN1PREFIX}/man/man1

.include <bsd.port.mk>
