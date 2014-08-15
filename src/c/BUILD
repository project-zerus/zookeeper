cc_library(
  name = 'zk',
  export_incs = './export_incs',
  incs = [
    '.',
    './include',
    './export_incs',
  ],
  warning = 'no',
  defs = [
    'THREADED',
  ],
  srcs = [
    'generated/zookeeper.jute.c',
    'src/recordio.c',
    'src/mt_adaptor.c',
    'src/winport.c',
    'src/zk_hashtable.c',
    'src/zk_log.c',
    'src/zookeeper.c',
    'src/hashtable/hashtable.c',
    'src/hashtable/hashtable_itr.c'
  ],
  deps = [
    '#pthread',
    '#rt',
  ]
)

cc_binary(
  name = 'cli',
  incs = [
    './include',
  ],
  defs = [
    'THREADED',
  ],
  srcs = 'src/cli.c',
  deps = ':zk',
)

cc_binary(
  name = 'load_gen',
  incs = [
    './include',
  ],
  defs = [
    'THREADED',
  ],
  extra_cppflags = [
    '-Wno-implicit-function-declaration'
  ],
  srcs = 'src/load_gen.c',
  deps = ':zk',
)
