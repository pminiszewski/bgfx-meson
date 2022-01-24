project('bgfx', 'cpp', 'c')

if(get_option('buildtype') == 'debug')
  add_project_arguments('-DBX_CONFIG_DEBUG=1', language: 'cpp')
else
  add_project_arguments('-DBX_CONFIG_DEBUG=0', language: 'cpp')
endif

add_project_arguments('-D__STDC_LIMIT_MACROS', '-D__STDC_FORMAT_MACROS', '-D__STDC_CONSTANT_MACROS', language: 'cpp')
add_project_arguments('/Zc:wchar_t', language: 'cpp')
subdir('meson/bx')
subdir('meson/bimg')
subdir('meson/bgfx')
subdir('meson/examples')
subdir('meson/tools')