macos_headers = subdir_glob([
  ('cmake-generated/macosx-x86_64/zzip', '**/*.h'),
]);

cxx_library(
  name = 'zzip',
  header_namespace = 'zzip',
  exported_headers = subdir_glob([
    ('zzip', '**/*.h'),
  ]),
  exported_platform_headers = [
    ('default', macos_headers),
    ('^macos.*', macos_headers),
  ],
  srcs = glob([
    'zzip/**/*.c',
  ]),
  visibility = [
    'PUBLIC',
  ],
)

cxx_library(
  name = 'zzipwrap',
  header_namespace = 'zzipwrap',
  exported_headers = subdir_glob([
    ('zzipwrap', '**/*.h'),
  ]),
  srcs = glob([
    'zzipwrap/**/*.c',
  ]),
  deps = [
    ':zzip',
  ],
  visibility = [
    'PUBLIC',
  ],
)
