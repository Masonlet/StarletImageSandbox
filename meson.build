project('starlet_image_sandbox', 'cpp',
  meson_version : '>=1.1',
  default_options : ['cpp_std=c++20']
)

sources = [
  'src/arg_parser.cpp',
  'src/ascii_converter.cpp',
  'src/image_loader.cpp',
  'src/main.cpp',
]

asset_dir = meson.current_source_dir() / 'assets'

if not get_option('build_local')
  starlet_serializer = subproject('starlet_serializer')
  serializer_dep = starlet_serializer.get_variable('starlet_serializer_dep')
else
  serializer_dep = dependency('starlet_serializer')
endif

executable('starlet_image_sandbox',
  sources,
  include_directories: 'inc',
  cpp_args: ['-DASSET_DIR="' + asset_dir + '"'],
  dependencies: serializer_dep,
)

