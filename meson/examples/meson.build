examples_root = '../../bgfx/examples/'


subdir('common')

if not get_option('with_bgfx_examples') 
subdir_done()
endif

executable('examples', [
  examples_root + '46-fsr/fsr.cpp',
  examples_root + '46-fsr/app.cpp',
  examples_root + '45-bokeh/bokeh.cpp',
  examples_root + '44-sss/screen_space_shadows.cpp',
  examples_root + '43-denoise/denoise.cpp',
  examples_root + '42-bunnylod/bunnylod.cpp',
  examples_root + '42-bunnylod/progmesh.c',
  examples_root + '41-tess/tess.cpp',
  examples_root + '40-svt/vt.cpp',
  examples_root + '40-svt/svt.cpp',
  examples_root + '39-assao/assao.cpp',
  examples_root + '38-bloom/bloom.cpp',
  examples_root + '37-gpudrivenrendering/gpudrivenrendering.cpp',
  examples_root + '36-sky/sky.cpp',
  examples_root + '35-dynamic/dynamic.cpp',
  examples_root + '34-mvs/mvs.cpp',
  examples_root + '33-pom/pom.cpp',
  examples_root + '32-particles/particles.cpp',
  examples_root + '31-rsm/reflectiveshadowmap.cpp',
  examples_root + '30-picking/picking.cpp',
  examples_root + '29-debugdraw/debugdraw.cpp',
  examples_root + '28-wireframe/wireframe.cpp',
  examples_root + '27-terrain/terrain.cpp',
  examples_root + '26-occlusion/occlusion.cpp',
  examples_root + '25-c99/helloworld.c',
  examples_root + '24-nbody/nbody.cpp',
  examples_root + '23-vectordisplay/vectordisplay.cpp',
  examples_root + '23-vectordisplay/main.cpp',
  examples_root + '22-windows/windows.cpp',
  examples_root + '21-deferred/deferred.cpp',
  examples_root + '20-nanovg/nanovg.cpp',
  examples_root + '19-oit/oit.cpp',
  examples_root + '18-ibl/ibl.cpp',
  examples_root + '16-shadowmaps/shadowmaps.cpp',
  examples_root + '15-shadowmaps-simple/shadowmaps_simple.cpp',
  examples_root + '14-shadowvolumes/shadowvolumes.cpp',
  examples_root + '13-stencil/stencil.cpp',
  examples_root + '12-lod/lod.cpp',
  examples_root + '11-fontsdf/fontsdf.cpp',
  examples_root + '10-font/font.cpp',
  examples_root + '09-hdr/hdr.cpp',
  examples_root + '08-update/update.cpp',
  examples_root + '07-callback/callback.cpp',
  examples_root + '06-bump/bump.cpp',
  examples_root + '05-instancing/instancing.cpp',
  examples_root + '04-mesh/mesh.cpp',
  examples_root + '03-raymarch/raymarch.cpp',
  examples_root + '02-metaballs/metaballs.cpp',
  examples_root + '01-cubes/cubes.cpp',
  examples_root + '00-helloworld/helloworld.cpp'
],
dependencies: [
  bx_dep,
  bimg_dep,
  bgfx_dep,
  example_glue_dep,
  examples_common_dep
],
link_args: [
  #'/entry:mainCRTStartup'
  
]
)