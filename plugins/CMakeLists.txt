set (plugins_available
  brieflz
  brotli
  bsc
  bzip2
  copy
  crush
  csc
  density
  doboz
  fari
  fastlz
  gipfeli
  heatshrink
  lz4
  lzf
  lzg
  lzham
  lzjb
  lzma
  lzo
  ms-compress
  ncompress
  pithy
  quicklz
  snappy
  wflz
  yalz77
  zlib
  zlib-ng
  zling
  zpaq
  zstd)

foreach (plugin ${plugins_available})
  string(TOUPPER ${plugin} plugin_uc_name)
  if (NOT "${ENABLE_${plugin_uc_name}}" STREQUAL "no")
    add_subdirectory (${plugin})
  endif()
endforeach(plugin)
