PORTNAME=	libgamepad
PORTVERSION=	0.1.2
PORTREVISION=	1
CATEGORIES=	devel games
MASTER_SITES=	http://acadix.biz/Ports/distfiles/

MAINTAINER=	jwb@FreeBSD.org
COMMENT=	Generic gamepad API

LICENSE=	BSD2CLAUSE

USES=		tar:xz

pre-build:
	(cd ${WRKSRC} && make depend)

MAKE_FLAGS+=	PREFIX=${STAGEDIR}${PREFIX} \
		MANPREFIX=${STAGEDIR}${PREFIX}/share

.include <bsd.port.mk>
