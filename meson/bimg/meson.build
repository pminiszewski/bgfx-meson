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

bimg_encode_lib = static_library('bimg_encode', [
bimg_root + '3rdparty/tinyexr/deps/miniz/miniz.c',
bimg_root + '3rdparty/pvrtc/PvrTcEncoder.cpp',
bimg_root + '3rdparty/pvrtc/PvrTcPacket.cpp',
bimg_root + '3rdparty/pvrtc/MortonTable.cpp',
bimg_root + '3rdparty/pvrtc/PvrTcDecoder.cpp',
bimg_root + '3rdparty/pvrtc/BitScale.cpp',
bimg_root + '3rdparty/nvtt/nvtt.cpp',
bimg_root + '3rdparty/nvtt/nvmath/fitting.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode7.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_utils.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode3.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode4.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode5.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode6.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode0.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode1.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl_mode2.cpp',
bimg_root + '3rdparty/nvtt/bc7/avpcl.cpp',
bimg_root + '3rdparty/nvtt/bc6h/zohone.cpp',
bimg_root + '3rdparty/nvtt/bc6h/zohtwo.cpp',
bimg_root + '3rdparty/nvtt/bc6h/zoh.cpp',
bimg_root + '3rdparty/nvtt/bc6h/zoh_utils.cpp',
bimg_root + '3rdparty/lodepng/lodepng.cpp',
bimg_root + '3rdparty/libsquish/singlecolourfit.cpp',
bimg_root + '3rdparty/libsquish/squish.cpp',
bimg_root + '3rdparty/libsquish/maths.cpp',
bimg_root + '3rdparty/libsquish/rangefit.cpp',
bimg_root + '3rdparty/libsquish/colourfit.cpp',
bimg_root + '3rdparty/libsquish/colourset.cpp',
bimg_root + '3rdparty/libsquish/clusterfit.cpp',
bimg_root + '3rdparty/libsquish/colourblock.cpp',
bimg_root + '3rdparty/libsquish/alpha.cpp',
bimg_root + '3rdparty/iqa/source/ssim.c',
bimg_root + '3rdparty/iqa/source/decimate.c',
bimg_root + '3rdparty/iqa/source/math_utils.c',
bimg_root + '3rdparty/iqa/source/ms_ssim.c',
bimg_root + '3rdparty/iqa/source/mse.c',
bimg_root + '3rdparty/iqa/source/psnr.c',
bimg_root + '3rdparty/iqa/source/convolve.c',
bimg_root + '3rdparty/etc2/ProcessRGB.cpp',
bimg_root + '3rdparty/etc2/Tables.cpp',
bimg_root + '3rdparty/etc1/etc1.cpp',
bimg_root + '3rdparty/edtaa3/edtaa3func.cpp',
bimg_root + '3rdparty/astc/mathlib.cpp',
bimg_root + '3rdparty/astc/softfloat.cpp',
bimg_root + '3rdparty/astc/astc_symbolic_physical.cpp',
bimg_root + '3rdparty/astc/astc_weight_align.cpp',
bimg_root + '3rdparty/astc/astc_weight_quant_xfer_tables.cpp',
bimg_root + '3rdparty/astc/astc_percentile_tables.cpp',
bimg_root + '3rdparty/astc/astc_pick_best_endpoint_format.cpp',
bimg_root + '3rdparty/astc/astc_quantization.cpp',
bimg_root + '3rdparty/astc/astc_kmeans_partitioning.cpp',
bimg_root + '3rdparty/astc/astc_lib.cpp',
bimg_root + '3rdparty/astc/astc_partition_tables.cpp',
bimg_root + '3rdparty/astc/astc_ideal_endpoints_and_weights.cpp',
bimg_root + '3rdparty/astc/astc_imageblock.cpp',
bimg_root + '3rdparty/astc/astc_integer_sequence.cpp',
bimg_root + '3rdparty/astc/astc_compute_variance.cpp',
bimg_root + '3rdparty/astc/astc_decompress_symbolic.cpp',
bimg_root + '3rdparty/astc/astc_encoding_choice_error.cpp',
bimg_root + '3rdparty/astc/astc_find_best_partitioning.cpp',
bimg_root + '3rdparty/astc/astc_color_quantize.cpp',
bimg_root + '3rdparty/astc/astc_color_unquantize.cpp',
bimg_root + '3rdparty/astc/astc_compress_symbolic.cpp',
bimg_root + '3rdparty/astc/astc_block_sizes2.cpp',
bimg_root + '3rdparty/astc/astc_averages_and_directions.cpp',
bimg_root + 'src/image_encode.cpp',
bimg_root + 'src/image_cubemap_filter.cpp',
],
include_directories: [
  bimg_root + 'include',
  bimg_root + '3rdparty',
  bimg_root + '3rdparty/nvtt',
  bimg_root + '3rdparty/iqa/include',
  bimg_root + '3rdparty/tinyexr/deps/miniz',
],
dependencies: bx_dep,
cpp_args: [
  '/wd4828',
]
)

bimg_dep = declare_dependency(
  include_directories: bimg_inc,
  link_with: [
    bimg_lib,
    bimg_decode_lib
  ]
)


