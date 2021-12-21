# static asset files to copy
index_sources = [
  'index.theme',
]

theme_variants = [
  'dark',
]

_communitheme_dir = join_paths(gtk_theme_dir, 'Adwaita-Ubuntu')
install_data(index_sources, install_dir: _communitheme_dir)
foreach variant: theme_variants
  _communitheme_dir = join_paths(gtk_theme_dir, 'Adwaita-Ubuntu-' + variant)
  install_data(index_sources, install_dir: _communitheme_dir)
endforeach

subdir('gtk-2.0')
subdir('gtk-3.0')
