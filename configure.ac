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

AC_INIT([Stationery],[develop])
AC_PREFIX_DEFAULT([/Preview])
AM_INIT_AUTOMAKE([foreign])
AM_MAINTAINER_MODE

AC_CHECK_PROG([ZIP],[zip],[zip])
if test x"$ZIP" = x""; then
	AC_MSG_ERROR([cannot locate the 'zip' utility required to build Talisker stationery])
fi

AC_CHECK_PROG([PRINT],[printf],[printf],[echo -n])

AC_CONFIG_FILES([
Makefile
Documents/Makefile
Documents/Blank/Makefile
])

AC_OUTPUT
