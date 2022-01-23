bimg_root = '../../bimg/'

bimg_inc = include_directories([
  bimg_root + 'include',
  bimg_root + '3rdparty',
  bimg_root + '3rdparty/astc-codec',
  bimg_root + '3rdparty/astc-codec/include',
  bimg_root + '3rdparty/tinyexr/deps/miniz',
])



bimg_lib = static_library('bimg', [
  bimg_root + '3rdparty/astc-codec/src/decoder/astc_file.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/codec.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/endpoint_codec.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/footprint.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/integer_sequence_codec.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/intermediate_astc_block.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/logical_astc_block.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/partition.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/physical_astc_block.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/quantization.cc',
  bimg_root + '3rdparty/astc-codec/src/decoder/weight_infill.cc',
  bimg_root + '3rdparty/tinyexr/deps/miniz/miniz.c',
  bimg_root + 'src/image.cpp',
  bimg_root + 'src/image_gnf.cpp'
],
include_directories: bimg_inc,
dependencies: [
  bx_dep
])

bimg_decode_lib = static_library('bimg_decode', [
  bimg_root + 'src/image_decode.cpp',
],
include_directories:  bimg_inc,
dependencies: bx_dep
)

bimg_dep = declare_dependency(
  include_directories: bimg_inc,
  link_with: [
    bimg_lib,
    bimg_decode_lib
  ]
)


