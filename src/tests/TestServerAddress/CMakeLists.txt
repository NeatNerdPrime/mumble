# Copyright 2020-2023 The Mumble Developers. All rights reserved.
# Use of this source code is governed by a BSD-style license
# that can be found in the LICENSE file at the root of the
# Mumble source tree or at <https://www.mumble.info/LICENSE>.

add_executable(TestServerAddress TestServerAddress.cpp)

set_target_properties(TestServerAddress PROPERTIES AUTOMOC ON)

target_link_libraries(TestServerAddress PRIVATE shared Qt6::Test)

add_test(NAME TestServerAddress COMMAND $<TARGET_FILE:TestServerAddress>)
