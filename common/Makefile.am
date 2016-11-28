themedarkerdir  = $(datadir)/themes/Arc-Capitan

ithemedarkerdir   = $(DESTDIR)$(themedarkerdir)

install-exec-hook:

install-data-local:

	$(MKDIR_P) $(ithemedarkerdir)
	cp $(srcdir)/index.theme $(ithemedarkerdir)/index.theme


if ENABLE_GTK2

	$(MKDIR_P) $(ithemedarkerdir)/gtk-2.0

	cd $(srcdir)/gtk-2.0 && cp -R \
		assets \
		menubar-toolbar \
		*.rc \
		$(ithemedarkerdir)/gtk-2.0

	cd $(srcdir)/gtk-2.0 && cp -R \
		gtkrc-darker \
		$(ithemedarkerdir)/gtk-2.0/gtkrc

endif # ENABLE_GTK2


if ENABLE_GTK3

	$(MKDIR_P) $(ithemedarkerdir)/gtk-3.0

	cd $(srcdir)/gtk-3.0 && cp thumbnail.png $(ithemedarkerdir)/gtk-3.0

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -R \
		assets \
		gtk-dark.css \
		$(ithemedarkerdir)/gtk-3.0

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -R \
		gtk-darker.css \
		$(ithemedarkerdir)/gtk-3.0/gtk.css

if !ENABLE_TRANSPARENCY

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -R \
		gtk-solid-darker.css \
		$(ithemedarkerdir)/gtk-3.0/gtk.css

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -R \
		gtk-solid-dark.css \
		$(ithemedarkerdir)/gtk-3.0/gtk-dark.css

endif #!ENABLE_TRANSPARENCY

endif # ENABLE_GTK3


if ENABLE_METACITY

	cp -R $(srcdir)/metacity-1 $(ithemedarkerdir)

	cd $(ithemedarkerdir)/metacity-1 && \
		mv metacity-theme-1-dark.xml metacity-theme-1.xml && \
		mv metacity-theme-2-dark.xml metacity-theme-2.xml && \
		mv thumbnail-dark.png thumbnail.png

endif # ENABLE_METACITY


if ENABLE_UNITY

	cp -R $(srcdir)/unity $(ithemedarkerdir)

	cd $(ithemedarkerdir)/unity

endif # ENABLE_UNITY


uninstall-local:
	rm -rf $(ithemedarkerdir)


EXTRA_DIST = $(srcdir)/gnome-shell \
	     $(srcdir)/gtk-2.0 \
	     $(srcdir)/gtk-3.0 \
	     $(srcdir)/metacity-1 \
	     $(srcdir)/unity \
	     $(srcdir)/index.theme
