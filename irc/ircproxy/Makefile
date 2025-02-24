PORTNAME=	ircproxy
PORTVERSION=	1.3.6
PORTREVISION=	3
CATEGORIES=	irc
MASTER_SITES=	https://BSDforge.com/projects/source/irc/ircproxy/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	IRC proxy/bouncer daemon
WWW=		http://ircproxy.sourceforge.net/

LICENSE=	GPLv3+
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		Unfetchable
DEPRECATED=	Abandonware, last release in 2010 and dead upstream. Consider using irc/soju or irc/znc
EXPIRATION_DATE=2024-02-29

LIB_DEPENDS=	libcares.so:dns/c-ares

USES=		autoreconf tar:bzip2
GNU_CONFIGURE=	yes
LDFLAGS+=	-L${LOCALBASE}/lib -lcrypto
CFLAGS+=	-I${LOCALBASE}/include

USERS=		ircproxyd
GROUPS=		ircproxyd

SUB_LIST=	IRC_USR=${USERS} IRC_GRP=${GROUPS}
SUB_FILES=	pkg-deinstall

OPTIONS_DEFINE=	SSL IPV6 MEMDEBUG FDDEBUG
OPTIONS_DEFAULT=	SSL MEMDEBUG FDDEBUG
MEMDEBUG_DESC=	Enable memory debugging
FDDEBUG_DESC=	Enable file descriptor debugging

MEMDEBUG_CONFIGURE_ENABLE=	memdebug
FDDEBUG_CONFIGURE_ENABLE=	fddebug
IPV6_CONFIGURE_ENABLE=		ipv6
SSL_CONFIGURE_ENABLE=		ssl
SSL_USES=		ssl

.include <bsd.port.pre.mk>

post-patch:
	@${REINPLACE_CMD} -e 's|EUSER="ircproxy"|EUSER="ircproxyd"|g; \
		s|EGROUP="users"|EGROUP="ircproxyd"|g' ${WRKSRC}/data/${PORTNAME}d.conf
	@${REINPLACE_CMD} -e '/gnutls/!s,SSL_library_init,OPENSSL_init_ssl,' \
		${WRKSRC}/configure.in

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/imkpasswd ${STAGEDIR}${PREFIX}/bin/ircproxyd

.include <bsd.port.post.mk>
