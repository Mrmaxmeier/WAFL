# Copyright 2021 Keno Hassler
# SPDX-License-Identifier: Apache-2.0

set(Sources
	wavm-afl.c)

set(PublicHeaders
	${WAVM_INCLUDE_DIR}/wavm-afl/wavm-afl.h)

WAVM_ADD_LIB_COMPONENT(wavm-afl
	SOURCES ${Sources} ${PublicHeaders}
	PRIVATE_LIB_COMPONENTS LLVMJIT Runtime)
