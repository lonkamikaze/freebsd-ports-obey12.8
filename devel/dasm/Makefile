# Created by: Uffe Jakobsen <uffe@uffe.org>
# $FreeBSD$

PORTNAME=	dasm
PORTVERSION=	2.20.11
CATEGORIES=	devel
MASTER_SITES=	SF/${PORTNAME}-dillon/${PORTNAME}-dillon/${PORTVERSION}

MAINTAINER=	uffe@uffe.org
COMMENT=	Macro assembler for 8-bit microprocessors including MOS 6502, MC6803

LICENSE=	GPLv2

BROKEN=		Does not fetch
OPTIONS_DEFINE=	DOCS

USES=	gmake

BUILD_WRKSRC=	${WRKSRC}/src
MAKE_ARGS=	CC=${CC:Q} LDFLAGS="${LDFLAGS}" CFLAGS="${CFLAGS}"

PORTDOCS=	*
PLIST_FILES=	bin/dasm \
		bin/ftohex

do-install:
.for filename in dasm ftohex
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/${filename} ${STAGEDIR}${PREFIX}/bin
.endfor
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/doc/* ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
