PORTNAME=	asciidoctor-epub3
PORTVERSION=	2.1.0
PORTREVISION=	1
CATEGORIES=	textproc rubygems
MASTER_SITES=	RG

MAINTAINER=	doceng@FreeBSD.org
COMMENT=	Convert AsciiDoc documents to EPUB3
WWW=		https://github.com/asciidoctor/asciidoctor-epub3

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	rubygem-asciidoctor>=2.0<3:textproc/rubygem-asciidoctor \
		rubygem-gepub>=1.0.0:textproc/rubygem-gepub \
		rubygem-mime-types>=3.0:misc/rubygem-mime-types \
		rubygem-mini_portile2>=2.8.2:devel/rubygem-mini_portile2 \
		rubygem-sass>0:textproc/rubygem-sass

USES=		gem

NO_ARCH=	yes

PLIST_FILES=	bin/asciidoctor-epub3

.include <bsd.port.mk>
