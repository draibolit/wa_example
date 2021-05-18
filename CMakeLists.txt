cmake_minimum_required(VERSION 3.9)
project(wa_example)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)



# Main target
add_executable(wa_example_factorial
			  "${PROJECT_SOURCE_DIR}/src/factorial.cpp"
			  "${PROJECT_SOURCE_DIR}/src/factorial-service.cpp"
			  )
target_include_directories(wa_example_factorial
						  PRIVATE ${PROJECT_SOURCE_DIR}/src
						  )

target_link_options(wa_example_factorial
	PRIVATE "-sEXPORTED_RUNTIME_METHODS=[ccall,cwrap]"
	PRIVATE "-sEXPORTED_FUNCTIONS=[_factorial]"
                          )
