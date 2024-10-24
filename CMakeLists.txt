# Copyright (C) 2022-2024 Trevor Last
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.

cmake_minimum_required(VERSION 3.13)

set(GLUTILS_VERSION_MAJOR 1)
set(GLUTILS_VERSION_MINOR 0)
set(GLUTILS_VERSION_PATCH 2)
set(GLUTILS_VERSION ${GLUTILS_VERSION_MAJOR}.${GLUTILS_VERSION_MINOR}.${GLUTILS_VERSION_PATCH})

project(GLUtils VERSION ${GLUTILS_VERSION} LANGUAGES CXX)


find_package(glm 1.0 REQUIRED)
find_package(GLEW REQUIRED)

add_subdirectory(glutils)
add_library(glutils::glutils ALIAS glutils)
