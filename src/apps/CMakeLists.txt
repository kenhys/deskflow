# Deskflow -- mouse and keyboard sharing utility
# Copyright (C) 2012-2024 Symless Ltd.
# Copyright (C) 2009-2012 Nick Bolton
#
# This package is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# found in the file LICENSE that should have accompanied this file.
#
# This package is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

option(BUILD_UNIFIED "Build unified binary" OFF)
if(BUILD_UNIFIED)
  add_subdirectory(deskflow-core)
else()
  add_subdirectory(deskflow-client)
  add_subdirectory(deskflow-server)
endif(BUILD_UNIFIED)

## Only used on windows
add_subdirectory(deskflow-daemon)

option(BUILD_GUI "Build GUI" ON)
if(BUILD_GUI)
  add_subdirectory(deskflow-gui)
endif(BUILD_GUI)
