PORTNAME=	wmii
DISTVERSION=	3.6	# this is stable version; for 3.9.x, use -devel port
PORTREVISION=	7
CATEGORIES=	x11-wm
MASTER_SITES=	http://dl.suckless.org/wmii/

MAINTAINER=	rodrigo@FreeBSD.org
COMMENT=	Dynamic, minimalist window manager for X11
WWW=		http://wmii.suckless.org/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libixp.so:devel/libixp
RUN_DEPENDS=	dmenu:x11/dmenu

USES=		xorg
USE_XORG=	x11 xorgproto xt xext

CONFLICTS=	wmii-devel

MAKE_ARGS=	PREFIX="${PREFIX}" MAN="${MANPREFIX}/man" \
		INCLUDE="${LOCALBASE}/include" \
		INCX11="-I${LOCALBASE}/include" \
		LIBX11="-L${LOCALBASE}/lib -lX11 -lixp" \
		CC="${CC} -c" LD="${CC}" LIBIXP="" STATIC=""

OPTIONS_DEFINE=	SLIM_LAYOUT_BOX UTF8
SLIM_LAYOUT_BOX_DESC=	Build with slim layout boxes

UTF8_USES=	iconv
UTF8_MAKE_ARGS=	LIBICONV="${ICONV_LIB}"
UTF8_MAKE_ARGS_OFF=	-DNO_UTF8

SLIM_LAYOUT_BOX_EXTRA_PATCHES=	${FILESDIR}/extra-patch-slim-layout-boxes

post-patch: .SILENT
	${REINPLACE_CMD} -e 's|-lfmt -lutf|$${LIBX11} & -lX11|' \
		${WRKSRC}/cmd/Makefile
	${REINPLACE_CMD} -e '/_XOPEN_SOURCE/d' ${WRKSRC}/cmd/wmii/dat.h
# Strip debug build options
	${REINPLACE_CMD} -E 's| -g( -O0)?||' ${WRKSRC}/config.mk
	${REINPLACE_CMD} -e 's|CFLAGS += -DIXPlint|& -DIXP_NEEDAPI=89|' \
		${WRKSRC}/config.mk
# Fix brain-damaged piece of code which breaks on arches where `size_t'
# is not 32-bit unsigned integer (e.g. amd64)
	${REINPLACE_CMD} -e '/wmii_strlcat/d' ${WRKSRC}/include/util.h
	${REINPLACE_CMD} -e 's|strlcat|wmii_&|' ${WRKSRC}/include/util.h \
		${WRKSRC}/cmd/util.c ${WRKSRC}/cmd/wmii/client.c

post-install:
.for f in wmii wmii9menu wmiir
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${f}
.endfor

.include <bsd.port.mk>
