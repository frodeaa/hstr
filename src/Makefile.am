# Makefile.am		HSTR automake
#
# Copyright (C) 2014  Martin Dvorak <martin.dvorak@mindforger.com>
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# http://mij.oltrelinux.com/devel/autoconf-automake/
AM_CFLAGS = --pedantic -Wall -std=c99 -O2
AM_LDFLAGS =

# bin_ installs to bin; hh_ is the binary name
bin_PROGRAMS = hh

hh_SOURCES = 						\
	hashset.c include/hashset.h 			\
	hstr_curses.c include/hstr_curses.h 		\
	hstr_history.c include/hstr_history.h 		\
	hstr_utils.c include/hstr_utils.h 		\
	hstr_favorites.c include/hstr_favorites.h	\
	hstr_blacklist.c include/hstr_blacklist.h	\
	hstr_regexp.c include/hstr_regexp.h		\
	radixsort.c include/radixsort.h 		\
	hstr.c 

# create hh > hstr hard link on installation
install-exec-hook:
	ln $(DESTDIR)$(bindir)/hh$(EXEEXT) $(DESTDIR)$(bindir)/hstr$(EXEEXT)

hh_LDADD = $(NCURSES_LIBS)
