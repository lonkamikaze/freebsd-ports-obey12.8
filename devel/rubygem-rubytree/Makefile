# Created by: Mikhail T. <m.tsatsenko@gmail.com>
# $FreeBSD$

PORTNAME=	rubytree
PORTVERSION=	0.9.7
CATEGORIES=	devel rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Implementation of the Tree data structure for the Ruby

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE.md

RUN_DEPENDS=	rubygem-json>=1.8:devel/rubygem-json \
		rubygem-structured_warnings>=0.2:devel/rubygem-structured_warnings

NO_ARCH=	yes
USE_RUBY=	yes
USE_RUBY_RDOC=	yes
USES=		gem

.include <bsd.port.mk>
