common_root = '../../../bgfx/examples/common/'
common_inc = include_directories([
  common_root,
  common_root + 'debugdraw',
  common_root + 'entry',
  common_root + 'font',
  common_root + 'imgui',
  common_root + 'nanovg',
  common_root + 'ps',
])

example_common_args = []
if get_option('use_entry').enabled()
  example_common_args += '-DUSE_ENTRY=1'
endif

example_common_lib = static_library('example-common', [
  common_root + 'debugdraw/debugdraw.cpp',
  common_root + 'entry/cmd.cpp',
  common_root + 'entry/dialog.cpp',
  common_root + 'entry/entry_android.cpp',
  common_root + 'entry/entry_glfw.cpp',
  common_root + 'entry/entry_html5.cpp',
  common_root + 'entry/entry_noop.cpp',
  common_root + 'entry/entry_sdl.cpp',
  common_root + 'entry/entry_windows.cpp',
  common_root + 'entry/entry_x11.cpp',
  common_root + 'entry/entry.cpp',
  common_root + 'entry/input.cpp',
  common_root + 'font/font_manager.cpp',
  common_root + 'font/text_buffer_manager.cpp',
  common_root + 'font/text_metrics.cpp',
  common_root + 'font/utf8.cpp',
  common_root + 'imgui/imgui.cpp',
  common_root + 'nanovg/nanovg_bgfx.cpp',
  common_root + 'nanovg/nanovg.cpp',
  common_root + 'ps/particle_system.cpp',
  common_root + 'bgfx_utils.cpp',
  common_root + 'camera.cpp',
  common_root + 'cube_atlas.cpp',
],
include_directories: common_inc,
cpp_args: example_common_args,
dependencies: [
  bx_dep,
  bimg_dep,
  bgfx_dep
])

examples_common_dep = declare_dependency(
  include_directories: common_inc,
  link_with: example_common_lib
)

example_glue_lib = static_library('example-glue', [
    common_root + 'example-glue.cpp'
],
dependencies: [
  bx_dep,
  bgfx_dep
],
)

example_glue_dep = declare_dependency(
  link_with: example_glue_lib
)