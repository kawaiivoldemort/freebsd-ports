PORTNAME=	knews
PORTVERSION=	1.0b.1
PORTREVISION=	15
CATEGORIES=	news
MASTER_SITES=	LOCAL/dinoex

MAINTAINER=	dinoex@FreeBSD.org
COMMENT=	Threaded NNTP newsreader for X11

LIB_DEPENDS=	libpng.so:graphics/png \
		libcompface.so:mail/faces
RUN_DEPENDS=	newsp:print/mp-letter

LICENSE=	GPLv2

USES=		imake jpeg xorg
USE_XORG=	xmu xpm xt sm ice xext x11
MAKE_FLAGS=	BINDIR=${PREFIX}/bin CC="${CC}" \
		XAPPLOADDIR=${PREFIX}/lib/X11/app-defaults  -f

.if defined(MAKE_JOBS)
MAKE_ARGS+=	-j${MAKE_JOBS}
.endif

.include <bsd.port.mk>
