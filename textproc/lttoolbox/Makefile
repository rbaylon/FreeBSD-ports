PORTNAME=	lttoolbox
DISTVERSION=	3.7.6
CATEGORIES=	textproc
MASTER_SITES=	https://github.com/apertium/${PORTNAME}/releases/download/v${DISTVERSION}/

MAINTAINER=	bofh@FreeBSD.org
COMMENT=	Tool for lexical, morphological analysis and generation of words
WWW=		https://wiki.apertium.org/wiki/Lttoolbox

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	utf8cpp>=4.0.3:devel/utf8cpp
LIB_DEPENDS=	libicuio.so:devel/icu \
		libxml2.so:textproc/libxml2

USES=		autoreconf compiler:c++14-lang libtool pathfix pkgconfig tar:bz2
USE_LDCONFIG=	yes

GNU_CONFIGURE=	yes

INSTALL_TARGET=	install-strip

CFLAGS+=	-I${LOCALBASE}/include/utf8cpp
LDFLAGS+=	-lpthread

.include <bsd.port.mk>
