cmake_minimum_required(VERSION 2.8)	 # �������� ������ CMake.
										# ���� ������ ������������ ���������
										# ������ ��������, ��������� ��������� �����.

project(hello_world)			# �������� �������

set(SOURCE_EXE Source/main.cpp)		# ��������� ���������� �� ������� ���������� ��� ������������ �����

set(SOURCE_LIB Source/foo.cpp)			# ���� �����, �� ��� ����������

add_library(foo STATIC ${SOURCE_LIB})	# �������� ����������� ���������� � ������ foo

add_executable(main ${SOURCE_EXE})	# ������� ����������� ���� � ������ main

target_link_libraries(main foo)		# �������� ��������� � �����������