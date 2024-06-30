project(
'bgfx', 
'cpp', 
'c', 
default_options: [
  'cpp_std=c++17'
])

add_project_arguments('-D__STDC_LIMIT_MACROS', '-D__STDC_FORMAT_MACROS', '-D__STDC_CONSTANT_MACROS', language: 'cpp')
add_project_arguments([
  '/Zc:wchar_t',
  '/Zc:__cplusplus',  # Enable updated __cplusplus macro.
	'/Zc:preprocessor', # Enable preprocessor conformance mode.
  ], language: ['cpp', 'c'])
subdir('meson/bx')
subdir('meson/bimg')
subdir('meson/bgfx')
if get_option('with_bgfx_examples') 
subdir('meson/examples')
endif
subdir('meson/tools')