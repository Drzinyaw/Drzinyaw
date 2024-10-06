- ame: Windows Builds

on:
  push:
    paths-ignore:
      - '**.md'
      - 'LICENSE'
      - 'Assets/**'
      - 'Docs/**'

  pull_request:
    paths-ignore:
      - '**.md'
      - 'LICENSE'
      - 'Assets/**'
      - 'Docs/**'

  workflow_dispatch:

env:
  PLATFORM_NAME: Win32
  BUILD_TYPE: RelWithDebInfo
  UPLOAD_ARTIFACT: true
  CACHE_DEPS: false
  FIXED_CMAKE_VERSION: 3.21.4

jobs:
  Build:
    runs-on: windows-latest
    runs-on: windows-2019

    defaults:
      run:
