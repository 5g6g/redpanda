
v_cc_library(
  NAME cloud_storage_clients
  SRCS
    client_pool.cc
    client_probe.cc
    s3_client.cc
    s3_error.cc
  DEPS
    Seastar::seastar
    v::bytes
    v::cloud_roles
    v::net
  DEFINES
    -DBOOST_ASIO_HAS_STD_INVOKE_RESULT
)
add_subdirectory(tests)
add_subdirectory(test_client)

