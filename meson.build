project(
  'CwAPI2D',
  version : '0.0.1',
  license : 'MIT',
  meson_version : '>=0.56.0',
)

cwapi2d_include_dir = include_directories('include')

cwapi2d_dep = declare_dependency(
  include_directories : cwapi2d_include_dir,
)

meson.override_dependency('CwAPI2D', cwapi2d_dep)
meson.override_dependency('cwapi2d', cwapi2d_dep)

install_subdir(
  'include/cwapi2d',
  install_dir : get_option('includedir'),
)

pkg = import('pkgconfig')

pkg.generate(
  name : meson.project_name(),
  filebase : 'cwapi2d',
  description : 'Cadwork 2D CwAPI2D plugin architecture C++ headers',
  version : meson.project_version(),
  subdirs : '.',
)
