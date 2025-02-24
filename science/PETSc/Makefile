PORTNAME=	PETSc
DISTVERSION=	3.20.2
PORTREVISION=	1
CATEGORIES=	science devel
MASTER_SITES=	http://web.cels.anl.gov/projects/petsc/download/release-snapshots/ # was: https://ftp.mcs.anl.gov/pub/petsc/release-snapshots/
DISTNAME=	${PORTNAME:tl}-${DISTVERSION}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Suite of data structures and routines from Argonne National Laboratory
WWW=		https://www.mcs.anl.gov/petsc

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	cmake:devel/cmake-core
LIB_DEPENDS=	libmpich.so:net/mpich

USES=		blaslapack fortran gmake python shebangfix xorg
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-shared-libraries=1 \
		--with-mpi-dir=${LOCALBASE} \
		--with-python=1 --with-python-pkg-config=${LOCALBASE}/libdata/pkgconfig \
		FCFLAGS="${FCFLAGS}" FFLAGS="${FCFLAGS}"	\
		${CONFIGURE_ARGS_${ARCH}} CPPFLAGS="${CPPFLAGS}" \
		AR=${AR} RANLIB=${RANLIB} \
		MAKEFLAGS="${MAKEFLAGS}" LDFLAGS="${LDFLAGS}" LIBS=""
CONFIGURE_ARGS_amd64=	CFLAGS="${CFLAGS} -msse2" CXXFLAGS="${CXXFLAGS} -msse2"
CONFIGURE_ARGS_i386=	CFLAGS="${CFLAGS} -msse2" CXXFLAGS="${CXXFLAGS} -msse2"
CONFIGURE_ARGS=	--with-64-bit-indices # as opposed to 32-bit indices that are default
CONFIGURE_LOG=	configure.log
USE_XORG=	x11
MAKEFILE=	makefile
SHEBANG_FILES=	configure lib/petsc/bin/*.py lib/petsc/bin/saws/SAWs.py lib/petsc/bin/saws/*.bash config/*.py	\
		lib/petsc/bin/petscnagfor share/petsc/chkerrconvert.py
USE_LDCONFIG=	yes
TEST_TARGET=	test # 152 of 11396 tests (1.3%) fail due to missing files like /usr/local/share/petsc/datafiles/meshes/square_periodic.msh (tests expect the packe to be installed)
BINARY_ALIAS=	python=${PYTHON_CMD}

LDFLAGS+=	${LOCALBASE}/lib/libmpi.so

DATADIR=	${PREFIX}/share/${PORTNAME:tl}
PLIST_SUB=	SHLIB=${DISTVERSION} SHL=${DISTVERSION:C/\.[0-9]$//}

OPTIONS_DEFINE=		METIS
OPTIONS_DEFAULT=	METIS

METIS_DESC=		Enable metis support for graph partitioning algorithms
METIS_CONFIGURE_ON=	--with-metis=1 # --with-parmetis=1 to use include/parmetis.h
METIS_LIB_DEPENDS=	libmetis.so:math/metis

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/libpetsc.so.${DISTVERSION}
	@${FIND} ${STAGEDIR}${PREFIX} -name "*.html" -delete
	@cd ${STAGEDIR}${PREFIX} && ${RM} -r bin/win32fe lib/petsc/conf/uninstall.py
	@${REINPLACE_CMD} -i '' -e 's|^PYTHON = .*|PYTHON = ${PYTHON_CMD}|' ${STAGEDIR}${PREFIX}/lib/petsc/conf/petscvariables
	@${REINPLACE_CMD} -i '' -e 's|#!/.*|#!${PYTHON_CMD}|' ${STAGEDIR}${PREFIX}/lib/petsc/conf/reconfigure-arch-*-c-debug.py
	@${RMDIR} ${STAGEDIR}${PREFIX}/lib/petsc/bin/__pycache__ # stray directory

# the file /usr/local/share/petsc/examples/config/gmakegen.py is expected by some dependencies, at least by math/slepc

.include <bsd.port.mk>
