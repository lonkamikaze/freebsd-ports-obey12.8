# Created by: Igor Pokrovsky <ip@doom.homeunix.org>
# $FreeBSD$

PORTNAME=	ensemblist
PORTVERSION=	040126
PORTREVISION=	10
CATEGORIES=	games
MASTER_SITES=	SAVANNAH

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Assemble given shapes from primitives

LIB_DEPENDS=	libmikmod.so:audio/libmikmod \
		libpng.so:graphics/png

USES=		gmake
USE_XORG=	xmu
USE_GL=		glut
MAKE_ARGS=	CC=${CC:Q} DATADIR="${DATADIR}"

PLIST_FILES=	bin/ensemblist man/man6/ensemblist.6.gz
PORTDATA=	*
PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin
	@${MKDIR} ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/datas/* ${STAGEDIR}${DATADIR}
	(cd ${WRKSRC}/html && ${COPYTREE_SHARE} . ${STAGEDIR}${DOCSDIR})
	${INSTALL_MAN} ${WRKSRC}/ensemblist.6 ${STAGEDIR}${MAN6PREFIX}/man/man6

.include <bsd.port.mk>
