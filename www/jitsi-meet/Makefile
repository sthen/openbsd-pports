COMMENT =	Web files for Jitsi Meet

CATEGORIES =	www

VERSION =	1.0.6542
MASTER_SITES =	https://download.jitsi.org/jitsi-meet/src/
PKGNAME =	jitsi-meet-${VERSION}
DISTNAME =	${PKGNAME}
EXTRACT_SUFX =	.tar.bz2

MAINTAINER =	Philipp Buehler <pb-openbsd@sysfive.com>, \
		Aisha Tammy <openbsd@aisha.cc>

# Apache-2.0
PERMIT_PACKAGE =	Yes

NO_BUILD =	Yes
NO_TEST =	Yes

PREFIX =	/var
INSTDIR =	${PREFIX}/www

post-extract:
	mv ${WRKDIR}/jitsi-meet/config.js ${WRKDIR}/jitsi-meet/config.js.sample
	mv ${WRKDIR}/jitsi-meet/interface_config.js ${WRKDIR}/jitsi-meet/interface_config.js.sample

do-install:
	${INSTALL_DATA_DIR} ${INSTDIR}
	cp -R ${WRKDIR}/jitsi-meet/ ${INSTDIR}


.include <bsd.port.mk>
