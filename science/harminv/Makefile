PORTNAME=	harminv
PORTVERSION=	1.3.1
PORTREVISION=	22
CATEGORIES=	science
MASTER_SITES=	http://ab-initio.mit.edu/harminv/

MAINTAINER=	devel@stasyan.com
COMMENT=	Solver of harmonic inversion
WWW=		http://ab-initio.mit.edu/wiki/index.php/Harminv

USES=		blaslapack fortran gmake libtool pathfix
GNU_CONFIGURE=	yes
USE_GCC=	yes
CPPFLAGS+=	-I${LOCALBASE}/include -fPIC
LD_LIBRARY_PATH=	-L${LOCALBASE}/lib -L/usr/lib
LDFLAGS+=	-L${LOCALBASE}/lib
CONFIGURE_ENV+=	LD_LIBRARY_PATH="${LD_LIBRARY_PATH}"
USE_LDCONFIG=	yes

.include <bsd.port.mk>
