# Created by: Juergen Lock <nox@FreeBSD.org>
# $FreeBSD$

PORTNAME=	m2vrequantiser
PORTVERSION=	1.1
CATEGORIES=	multimedia
MASTER_SITES=	http://launchpadlibrarian.net/52366061/
DISTNAME=	M2VRequantiser-v${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Requantize MPEG-2 streams without recompressing

PATCH_STRIP=	-p1
CFLAGS+=	-Duint=unsigned
MAKE_ARGS+=	CC=${CC:Q} CXX=${CXX:Q}
PLIST_FILES+=	bin/M2VRequantiser

post-patch:
	${REINPLACE_CMD} 's|$$(PREFIX)|$${DESTDIR}$$(PREFIX)|' ${WRKSRC}/Makefile

.include <bsd.port.mk>
