project(
  'CwAPI2DR',
  version : '0.0.1',
  license : 'MIT',
  meson_version : '>=0.56.0',
)

cwapi2dr_include_dir = include_directories('include')

cwapi2dr_dep = declare_dependency(
  include_directories : cwapi2dr_include_dir,
)

meson.override_dependency('CwAPI2DR', cwapi2dr_dep)
meson.override_dependency('cwapi2dr', cwapi2dr_dep)

install_subdir(
  'include/cwapi2dr',
  install_dir : get_option('includedir'),
)

pkg = import('pkgconfig')

pkg.generate(
  name : meson.project_name(),
  filebase : 'cwapi2dr',
  description : 'Cadwork 2DR CwAPI2DR plugin architecture C++ headers',
  version : meson.project_version(),
  subdirs : '.',
)
