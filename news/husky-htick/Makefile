PORTNAME=	husky-htick

COMMENT=	Husky FTN file ticker

LICENSE=	GPLv2

LIB_DEPENDS=	libareafix.so:news/husky-areafix \
		libfidoconfig.so:news/husky-fidoconf \
		libhusky.so:news/husky-huskylib \
		libsmapi.so:news/husky-smapi

ALL_TARGET=	all
INSTALL_TARGET=	install
USE_LDCONFIG=	yes
PLIST_FILES=	bin/htick share/man/man1/htick.1.gz

MASTERDIR=	${.CURDIR}/../husky
COMPONENT_SUBDIR=htick

# Settings below are required to handle texi output (html, INFO page)
USES+=			makeinfo
ALL_TARGET+=		doc
INSTALL_TARGET+=	install-doc
PORTDOCS=		htick.html
DOCSDIR=		${PREFIX}/share/doc/husky
INFO=			htick
MAKE_ARGS=		INFODIR=${PREFIX}/${INFO_PATH}

CFLAGS+=		-fcommon # fix build failure with clang-11 on 13-CURRENT

OPTIONS_DEFINE=	DOCS

.include "${MASTERDIR}/Makefile"
