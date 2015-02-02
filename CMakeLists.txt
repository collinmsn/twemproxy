cmake_minimum_required(VERSION 2.8.4)
project(twemproxy)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories("src/")

set(SOURCE_FILES
    src/event/nc_epoll.c
    src/event/nc_event.h
    src/event/nc_evport.c
    src/event/nc_kqueue.c
    src/hashkit/nc_crc16.c
    src/hashkit/nc_crc32.c
    src/hashkit/nc_fnv.c
    src/hashkit/nc_hashkit.h
    src/hashkit/nc_hsieh.c
    src/hashkit/nc_jenkins.c
    src/hashkit/nc_ketama.c
    src/hashkit/nc_md5.c
    src/hashkit/nc_modula.c
    src/hashkit/nc_murmur.c
    src/hashkit/nc_one_at_a_time.c
    src/hashkit/nc_random.c
    src/proto/nc_memcache.c
    src/proto/nc_proto.h
    src/proto/nc_redis.c
    src/nc.c
    src/nc_array.c
    src/nc_array.h
    src/nc_client.c
    src/nc_client.h
    src/nc_conf.c
    src/nc_conf.h
    src/nc_connection.c
    src/nc_connection.h
    src/nc_core.c
    src/nc_core.h
    src/nc_log.c
    src/nc_log.h
    src/nc_mbuf.c
    src/nc_mbuf.h
    src/nc_message.c
    src/nc_message.h
    src/nc_proxy.c
    src/nc_proxy.h
    src/nc_queue.h
    src/nc_rbtree.c
    src/nc_rbtree.h
    src/nc_request.c
    src/nc_response.c
    src/nc_server.c
    src/nc_server.h
    src/nc_signal.c
    src/nc_signal.h
    src/nc_stats.c
    src/nc_stats.h
    src/nc_string.c
    src/nc_string.h
    src/nc_util.c
    src/nc_util.h)

add_executable(twemproxy ${SOURCE_FILES})