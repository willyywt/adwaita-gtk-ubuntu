# Work around meson weakness: meson won't allow us to rename custom_target's output during install
variant_2 = 'dark'
input_scss = 'gtk-' + variant_2 + '.scss'
# PWD is <gitrepo>/build
command = 'cd ../Adwaita-Ubuntu/gtk-3.0; sassc -a ' + input_scss + ' ../../build/Adwaita-Ubuntu/gtk-3.0/dark/gtk.css'
custom_target('generate_' + 'gtk-' + variant_2,
  output: 'gtk.css',
  depend_files: gtk3_scss_dependencies,
  command: [bash, '-c', command],
  build_by_default: true,
  install: true,
  install_dir: gtk3_install_dir,
)
