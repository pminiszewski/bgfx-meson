bx_root = '../../bx/'
bx_inc = include_directories([
  bx_root + 'include',
  bx_root + 'include/compat/msvc', 
  #'include/tinystl',
  bx_root + '3rdparty/',
])
add_global_arguments(
  [
'-D__STDC_LIMIT_MACROS',
'-D__STDC_FORMAT_MACROS',
'-D__STDC_CONSTANT_MACROS',
  ], language : 'cpp')

 msvc_compiler = meson.get_compiler('cpp')

bx_lib = static_library('bx', [
  bx_root + 'src/allocator.cpp',
  bx_root + 'src/bounds.cpp',
  bx_root + 'src/bx.cpp',
  bx_root + 'src/commandline.cpp',
  bx_root + 'src/crtnone.cpp',
  bx_root + 'src/debug.cpp',
  bx_root + 'src/dtoa.cpp',
  bx_root + 'src/easing.cpp',
  bx_root + 'src/file.cpp',
  bx_root + 'src/filepath.cpp',
  bx_root + 'src/hash.cpp',
  bx_root + 'src/math.cpp',
  bx_root + 'src/mutex.cpp',
  bx_root + 'src/os.cpp',
  bx_root + 'src/process.cpp',
  bx_root + 'src/semaphore.cpp',
  bx_root + 'src/settings.cpp',
  bx_root + 'src/sort.cpp',
  bx_root + 'src/string.cpp',
  bx_root + 'src/thread.cpp',
  bx_root + 'src/timer.cpp',
  bx_root + 'src/url.cpp',
],
include_directories: bx_inc,
dependencies: [
 msvc_compiler.find_library('psapi'),
 msvc_compiler.find_library('gdi32'),
 msvc_compiler.find_library('DelayImp'),
]
)

bx_dep = declare_dependency(
  include_directories: bx_inc,
  link_with: bx_lib
)