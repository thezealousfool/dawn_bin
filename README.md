# dawn_bin

This repo is just a GitHub action file that tries to build dawn -- Google's
implementation of the [WebGPU Specification](https://www.w3.org/TR/webgpu/)
shipped in Google Chrome/Chromium browser. This repo specifically builds static
libraries for the native implementation of dawn to be run outside of the browser.

## Supported Platforms:

- macOS ARM (aarch64) ✅
- macOS Intel (x86_64) ✅
- linux ARM (aarch64) ✅
- linux x64 (x86_64) ✅
- windows ARM (aarch64) ❌ - PRs welcomed
- windows x64 (x86_64) ❌ - PRs welcomed

## Sample link command

macOS:

```bash
clang++ -o main_dawn_release -O3 glfw-release/lib/libglfw3.a webgpu-dawn-release/lib/libwebgpu_dawn.a webgpu-dawn-release/lib/libdawn_native_static.a webgpu-dawn-release/lib/libdawn_platform_static.a -x objective-c main.c -I glfw-release/include -I webgpu-dawn-release/include -framework CoreFoundation -framework Cocoa -framework IOKit -framework Metal -framework QuartzCore -framework IOSurface -framework Security
```

For GLFW static libraries checkout: [glfw_bin](https://github.com/thezealousfool/glfw_bin)
