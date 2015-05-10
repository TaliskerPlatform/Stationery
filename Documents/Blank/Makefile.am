## Copyright 2015 Mo McRoberts.
##
##  Licensed under the Apache License, Version 2.0 (the "License");
##  you may not use this file except in compliance with the License.
##  You may obtain a copy of the License at
##
##      http://www.apache.org/licenses/LICENSE-2.0
##
##  Unless required by applicable law or agreed to in writing, software
##  distributed under the License is distributed on an "AS IS" BASIS,
##  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
##  See the License for the specific language governing permissions and
##  limitations under the License.

stationerydir = $(prefix)/Stationery/Basic

noinst_DATA = Blank.zip

CLEANFILES = $(noinst_DATA) mimetype

MIMETYPE = application/vnd.oasis.opendocument.text-template

dist_noinst_DATA = META-INF/manifest.xml manifest.rdf \
	meta.xml content.xml styles.xml \
	Thumbnails/thumbnail.png

$(noinst_DATA): $(dist_noinst_DATA)
	rm -f $@ mimetype
	$(PRINT) '$(MIMETYPE)' > mimetype
	$(ZIP) -0 -X -D $@ mimetype
	$(ZIP) -9 -X -D $@ $+

# Use a hook to install because make has problems with spaces in filenames
install-data-hook:
	$(MKDIR_P) "$(DESTDIR)$(stationerydir)"
	$(INSTALL_DATA) $(noinst_DATA) "$(DESTDIR)$(stationerydir)/Blank document.ott"
