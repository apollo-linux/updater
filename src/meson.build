updater_sources = [
  'main.vala',
  'application.vala',
  'window.vala',
]

updater_deps = [
  config_dep,
  dependency('gtk4'),
  dependency('libadwaita-1', version: '>= 1.4'),
]

blueprints = custom_target('blueprints',
  input: files(
    'shortcuts-dialog.blp',
    'window.blp',
  ),
  output: '.',
  command: [find_program('blueprint-compiler'), 'batch-compile', '@OUTPUT@', '@CURRENT_SOURCE_DIR@', '@INPUT@'],
)


updater_sources += gnome.compile_resources('updater-resources',
  'updater.gresource.xml',
  dependencies: blueprints,
  c_name: 'updater'
)

executable('updater', updater_sources,
  dependencies: updater_deps,
  include_directories: config_inc,
       install: true,
)