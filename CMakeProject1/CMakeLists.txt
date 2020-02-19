# CMakeList.txt: CMakeProject1에 대한 CMake 프로젝트, 여기에 소스를 포함하고
# 프로젝트 특정 논리를 정의합니다.
#
cmake_minimum_required (VERSION 3.8)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

include_directories($ENV{UniversalCRTSdkDir}/Include/ucrt)
#include_directories($ENV{UniversalCRTSdkDir}/Include/10.0.10056.0/ucrt)

# 이 프로젝트의 실행 파일에 소스를 추가합니다.
add_executable (CMakeProject1 WIN32 
	"WindowsProject1.cpp" 
	"WindowsProject1.h" 
	"Resource.h" 
	"targetver.h" 
	"framework.h" 
	"WindowsProject1.rc" 
	"WindowsProject1.ico" 
	"small.ico" 
)

add_executable (CMakeProject3 WIN32 
	"WindowsProject1.cpp" 
	"WindowsProject1.rc" 
)

# TODO: 필요한 경우 테스트를 추가하고 대상을 설치합니다.
