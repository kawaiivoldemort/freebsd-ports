PORTNAME=	bkmrkconv
PORTVERSION=	1.12
CATEGORIES=	www
MASTER_SITES=	http://www.bleb.org/software/bkmrkconv/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Netscape bookmarks.html converter
WWW=		http://www.bleb.org/software/bkmrkconv/

LICENSE=	ART10

DEPRECATED=	Obsolete utility, generated files are already in a readable format
EXPIRATION_DATE=2024-05-31

USES=		perl5
NO_BUILD=	yes
NO_ARCH=	yes

OPTIONS_DEFINE=	DOCS

post-patch:
	@${FIND} ${WRKSRC} -type f -name '*.pl' | ${XARGS} ${REINPLACE_CMD} -i '' -e \
		's|/usr/bin/perl|${PERL}|g ; \
		 s|%%PREFIX%%|${PREFIX}|g'

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/bkmrkconv.pl \
		${STAGEDIR}${PREFIX}/bin/bkmrkconv
	@${MKDIR} ${STAGEDIR}${DATADIR}
	${INSTALL_SCRIPT} ${WRKSRC}/utils/* ${STAGEDIR}${DATADIR}
	@${MKDIR} ${STAGEDIR}${DATADIR}/src
	${INSTALL_DATA} ${WRKSRC}/src.example/* ${STAGEDIR}${DATADIR}/src

do-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README.txt ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
