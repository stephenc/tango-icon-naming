
bin_SCRIPTS = icon-name-mapping

%: %.pl.in
	sed -e "s#\@PERL\@#$(PERL)#g"		\
	    -e "s#\@DATADIR\@#$(pkgdatadir)#g"	\
	< $< > $@

dtddir = $(datadir)/dtds
dtd_DATA = legacy-icon-mapping.dtd

pkgdata_DATA = legacy-icon-mapping.xml

EXTRA_DIST =				\
	icon-name-mapping.pl.in		\
	$(dtd_DATA)			\
	$(pkgdata_DATA)

CLEANFILES =				\
	$(noinst_SCRIPTS)		\
	$(bin_SCRIPTS)

MAINTAINERCLEANFILES =			\
	Makefile.in			\
	aclocal.m4			\
	config.guess			\
	config.sub			\
	configure			\
	depcomp				\
	install-sh			\
	missing



