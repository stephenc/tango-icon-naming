
libexec_SCRIPTS = icon-name-mapping

%: %.pl.in
	sed -e "s#\@PERL\@#$(PERL)#g"		\
	    -e "s#\@DATADIR\@#$(pkgdatadir)#g"	\
	< $< > $@

%.pc: %.pc.in
	sed -e "s#\@program_path\@#$(libexecdir)#g" \
            -e "s#\@VERSION\@#$(VERSION)#g" < $< > $@

pkgconfig_in_files = icon-naming-utils.pc.in
pkgconfigdir = $(datadir)/pkgconfig
pkgconfig_DATA = $(pkgconfig_in_files:.pc.in=.pc)

dtddir = $(datadir)/dtds
dtd_DATA = legacy-icon-mapping.dtd

pkgdata_DATA = legacy-icon-mapping.xml

EXTRA_DIST =				\
	icon-name-mapping.pl.in		\
	$(pkgconfig_in_files)		\
	$(dtd_DATA)			\
	$(pkgdata_DATA)

CLEANFILES =				\
	$(pkgconfig_DATA)		\
	$(libexec_SCRIPTS)

MAINTAINERCLEANFILES =			\
	Makefile.in			\
	aclocal.m4			\
	config.guess			\
	config.sub			\
	configure			\
	depcomp				\
	install-sh			\
	missing

