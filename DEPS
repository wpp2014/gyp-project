vars = {
  'git_url': 'https://chromium.googlesource.com',
}

deps = {
}

hooks = [
  {
    'action': [
      'python',
      'src/tools/clang/scripts/update.py',
      '--if-needed'
    ],
    'pattern': '.',
    'name': 'clang'
  },
  {
    'action': [
      'python',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--running-as-hook'
    ],
    'pattern': '.',
    'name': 'sysroot'
  },
  {
    'action': [
      'python',
      'src/third_party/binutils/download.py'
    ],
    'pattern': '.',
    'name': 'binutils'
  },
  {
    'action': [
      'download_from_google_storage',
      '--no_resume',
      '--platform=linux*',
      '--no_auth',
      '--bucket',
      'chromium-eu-strip',
      '-s',
      'src/build/linux/bin/eu-strip.sha1'
    ],
    'pattern': '.',
    'name': 'eu-strip'
  }
]
