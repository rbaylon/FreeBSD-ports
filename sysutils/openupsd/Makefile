PORTNAME=	openupsd
PORTVERSION=	0.3.1
PORTREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	https://BSDforge.com/projects/source/sysutils/openupsd/

MAINTAINER=	tdb@FreeBSD.org
COMMENT=	UPS daemon for some Belkin UPS's
WWW=		https://BSDforge.com/projects/sysutils/openupsd/

BROKEN=		Unfetchable

USE_RC_SUBR=	${PORTNAME}
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--program-transform-name= --bindir=${PREFIX}/sbin

PLIST_FILES=	sbin/openupsd etc/openupsd.conf.sample

post-install:
	${INSTALL_DATA} ${WRKSRC}/openupsd.conf ${STAGEDIR}${PREFIX}/etc/openupsd.conf.sample

.include <bsd.port.mk>
