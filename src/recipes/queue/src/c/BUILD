cc_library(
  name = 'zk_queue',
  warning = 'no',
  export_incs = './include',
  srcs = [
    'src/zoo_queue.c',
  ],
  deps = '//zookeeper:zookeeper'
)

cc_binary(
  name = 'zk_queue_test',
  warning = 'no',
  srcs = [
    'tests/TestClient.cc',
    'tests/TestDriver.cc',
    'tests/Util.cc'
  ],
  deps = [
    ':zk_queue',
    '//cppunit:cppunit',
  ],
)
