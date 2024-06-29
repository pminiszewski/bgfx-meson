bgfx_root = '../../bgfx/'
shader_inc = [meson.current_source_dir() / bgfx_root / 'src', meson.current_source_dir() / bgfx_root / 'src/varying.def.sc']
bgfx_inc = include_directories([
  bgfx_root + 'include',
  bgfx_root + '3rdparty',
  bgfx_root + '3rdparty/directx-headers/include',
  bgfx_root + '3rdparty/directx-headers/include/directx',
  bgfx_root + '3rdparty/khronos',

])

bgfx_lib = static_library('bgfx', [
  bgfx_root + 'src/amalgamated.cpp',
],
include_directories: bgfx_inc,
dependencies: [
  bx_dep,
  bimg_dep
]
)

dear_imgui_lib = static_library('imgui',[
bgfx_root + '3rdparty/dear-imgui/imgui_demo.cpp',
bgfx_root + '3rdparty/dear-imgui/imgui_draw.cpp',
bgfx_root + '3rdparty/dear-imgui/imgui_tables.cpp',
bgfx_root + '3rdparty/dear-imgui/imgui_widgets.cpp',
bgfx_root + '3rdparty/dear-imgui/imgui.cpp'
],
include_directories: bgfx_inc,
cpp_args: [
  '/wd4828',
],
dependencies: [
  bx_dep,
  bimg_dep
])

meshoptimizer_lib = static_library('meshoptimizer', [
bgfx_root + '3rdparty/meshoptimizer/src/allocator.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/clusterizer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/indexcodec.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/indexgenerator.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/overdrawanalyzer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/overdrawoptimizer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/simplifier.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/spatialorder.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/stripifier.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vcacheanalyzer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vcacheoptimizer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vertexcodec.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vertexfilter.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vfetchanalyzer.cpp',
bgfx_root + '3rdparty/meshoptimizer/src/vfetchoptimizer.cpp',
])

bgfx_dep = declare_dependency(
  link_with: [
    bgfx_lib,
    dear_imgui_lib,
    meshoptimizer_lib
  ],
  include_directories: bgfx_inc
)

