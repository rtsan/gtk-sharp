TARGETS = MountOperation.exe 

DEBUGS = $(addsuffix .mdb, $(TARGETS))

assemblies = 					\
	$(top_builddir)/glib/glib-sharp.dll 	\
	$(top_builddir)/cairo/cairo-sharp.dll 	\
	$(top_builddir)/gtk/gtk-sharp.dll 	\
	$(top_builddir)/gio/gio-sharp.dll 	\
	$(top_builddir)/gdk/gdk-sharp.dll	\
	$(top_builddir)/pango/pango-sharp.dll	\
	$(top_builddir)/atk/atk-sharp.dll

references=$(addprefix -r:, $(assemblies))

noinst_SCRIPTS = $(TARGETS)
CLEANFILES = $(TARGETS) $(DEBUGS)

.cs.exe: $(assemblies)
	$(CSC) $(CSFLAGS) /out:$@ $(references) $<

EXTRA_DIST = 				\
	MountOperation.cs

