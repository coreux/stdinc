## Copyright 2013 Mo McRoberts.
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
##

EXTRA_DIST = regen-acinclude.m4

SUBDIRS = ux sys t .

include_HEADERS = \
	stdarg.h stdbool.h stddef.h stdint.h

dist_doc_DATA = README LICENSE-2.0 \
	stdarg.3.xml stdarg.3.html
dist_man3_MANS = stdarg.3

stdarg.3: stdarg.3.xml
	$(XML2MAN) $<
stdarg.3.html: stdarg.3.xml
	$(XML2HTML) $< > $@

tests: all
	t/cdefs-1
	t/stdarg-1
	t/stdbool-1
	t/stddef-1
	t/stdint-1
	t/types-1
