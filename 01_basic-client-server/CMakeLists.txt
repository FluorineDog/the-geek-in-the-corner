project(rdma_bas)
cmake_minimum_required(VERSION 2.8)
#add_library(rdma_basis)
set(LIBS rdmacm ibverbs pthread)
add_executable(server server.c)
add_executable(client client.c)
target_link_libraries(server ${LIBS})
target_link_libraries(client ${LIBS})