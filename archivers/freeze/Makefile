# Created by: lukin@okbmei.msk.su
# $FreeBSD$

PORTNAME=	freeze
PORTVERSION=	2.5
PORTREVISION=	2
CATEGORIES=	archivers
MASTER_SITES=	ftp://ftp.warwick.ac.uk/pub/compression/ \
		http://www.rebootking.de/distfiles/ \
		http://ngsoftwareltd.com/freebsd/distfiles/

MAINTAINER=	gabor@FreeBSD.org
COMMENT=	Compression program - often used in QNX

GNU_CONFIGURE=	yes
ALL_TARGET=	prog

MAKE_ARGS+=	CFLAGS="${CFLAGS} -I. -DCOMPAT" CC=${CC:Q}

PORTDOCS=	README

OPTIONS_DEFINE=	DOCS

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
