# Copyright 2020 Lawrence Livermore National Security, LLC and other CLIPPy
# Project Developers. See the top-level COPYRIGHT file for details.
#
# SPDX-License-Identifier: MIT

if (NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Debug)
endif()

set(CMAKE_CXX_FLAGS_DEBUG "-Wall -Wextra -pedantic -Wno-unused-parameter -O0 -g")
set(CMAKE_CXX_FLAGS_RELEASE "-Wall -Wextra -O3 -march=native")

# include_directories(${Boost_INCLUDE_DIRS})

include_directories(${PROJECT_SOURCE_DIR}/src/MetallJsonLines/)
include_directories(${PROJECT_SOURCE_DIR}/src/MetallGraph/)

add_metalldata_executable(mg-cc mg-cc.cpp)
setup_metall_target(mg-cc)
setup_ygm_target(mg-cc)
setup_clippy_target(mg-cc)

add_metalldata_executable(mg-init mg-init.cpp)
setup_metall_target(mg-init)
setup_ygm_target(mg-init)
setup_clippy_target(mg-init)

add_metalldata_executable(mg-read_vertices mg-read_vertices.cpp)
setup_metall_target(mg-read_vertices)
setup_ygm_target(mg-read_vertices)
setup_clippy_target(mg-read_vertices)

add_metalldata_executable(mg-read_edges mg-read_edges.cpp)
setup_metall_target(mg-read_edges)
setup_ygm_target(mg-read_edges)
setup_clippy_target(mg-read_edges)

add_metalldata_executable(mg-getitem mg-getitem.cpp)
setup_metall_target(mg-getitem)
setup_ygm_target(mg-getitem)
setup_clippy_target(mg-getitem)

add_metalldata_executable(mg-count mg-count.cpp)
setup_metall_target(mg-count)
setup_ygm_target(mg-count)
setup_clippy_target(mg-count)

add_metalldata_executable(mg-count_lines mg-count_lines.cpp)
setup_metall_target(mg-count_lines)
setup_ygm_target(mg-count_lines)
setup_clippy_target(mg-count_lines)

add_metalldata_executable(mg-kcore mg-kcore.cpp)
setup_metall_target(mg-kcore)
setup_ygm_target(mg-kcore)
setup_clippy_target(mg-kcore)

add_metalldata_executable(mg-bfs mg-bfs.cpp)
setup_metall_target(mg-bfs)
setup_ygm_target(mg-bfs)
setup_clippy_target(mg-bfs)


add_metalldata_executable(parquet_bench parquet_bench.cpp)
setup_metall_target(parquet_bench)
setup_ygm_target(parquet_bench)
setup_clippy_target(parquet_bench)

#~ add_metalldata_executable(mg-head mg-head.cpp)
#~ setup_metall_target(mg-head)
#~ setup_ygm_target(mg-head)
#~ setup_clippy_target(mg-head)

#~ add_metalldata_executable(mg-set mg-set.cpp)
#~ setup_metall_target(mg-set)
#~ setup_ygm_target(mg-set)
#~ setup_clippy_target(mg-set)

#~ add_metalldata_executable(mg-merge mg-merge.cpp)
#~ setup_metall_target(mg-merge)
#~ setup_ygm_target(mg-merge)
#~ setup_clippy_target(mg-merge)

#~ add_metalldata_executable(mg-clear mg-clear.cpp)
#~ setup_metall_target(mg-clear)
#~ setup_ygm_target(mg-clear)
#~ setup_clippy_target(mg-clear)


#~ add_metalldata_executable(mg-info mg-info.cpp)
#~ setup_metall_target(mg-info)
#~ setup_ygm_target(mg-info)
#~ setup_clippy_target(mg-info)

#~ add_metalldata_executable(rep rep.cpp)
#~ setup_metall_target(rep)
#~ setup_ygm_target(rep)
#~ setup_clippy_target(rep)

