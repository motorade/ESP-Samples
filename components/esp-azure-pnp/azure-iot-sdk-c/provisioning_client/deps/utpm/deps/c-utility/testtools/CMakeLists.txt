#Copyright (c) Microsoft. All rights reserved.
#Licensed under the MIT license. See LICENSE file in the project root for full license information.

#this is CMakeLists for testtools. It does nothing, except loads other folders

include("../configs/azure_c_shared_utilityFunctions.cmake")

usePermissiveRulesForSamplesAndTests()

if(NOT ${use_installed_dependencies})
    add_subdirectory(ctest)
    add_subdirectory(testrunner)
endif()

add_subdirectory(sal)
add_subdirectory(micromock)
