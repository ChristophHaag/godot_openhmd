project('godot_openhmd', 'c')
cc = meson.get_compiler('c')
dep_dl = cc.find_library('dl')
dep_ohmd = dependency('openhmd')
inc_glad = include_directories('./glad')
inc_godot = include_directories('../godot/modules/gdnative/include')
sources = [
  'src/godot_openhmd.c',
  'src/openhmd_shader.c',
  'src/openhmd_shader.h',
  'glad/glad.c'
]
shared_library(
  'godot_openhmd',
  sources,
  dependencies : [
    dep_ohmd,
    dep_dl
  ],
  include_directories : [
    inc_glad,
    inc_godot
  ]
)
