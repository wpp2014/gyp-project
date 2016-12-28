vars = {
  'git_url': 'https://chromium.googlesource.com',
}

deps = {
  'src/build':
      Var('git_url') + '/chromium/src/build.git@c45f365b10efe5057a01029f2d9d8bdfb13bc257',
  'src/third_party/binutils':
      Var('git_url') + '/chromium/src/third_party/binutils.git@8d77853bc9415bcb7bb4206fa2901de7603387db',
  'src/tools/clang':
      Var('git_url') + '/chromium/src/tools/clang.git@70184647b4240e4e7b38290ad3e049242a0dc0bc',
  'src/tools/gyp':
      Var('git_url') + '/external/gyp.git@940a15ee3f1c89f193cb4c19373b3f6e9ad15b95',
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
  }
]
