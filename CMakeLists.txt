
cmake_minimum_required(VERSION 3.1)


set(source 
async.c
hiredis.c
net.c
read.c
sds.c
)

add_library(hiredis STATIC ${source})

target_include_directories(hiredis PUBLIC .)

add_executable(example examples/example.c )

target_link_libraries(example PUBLIC hiredis)
