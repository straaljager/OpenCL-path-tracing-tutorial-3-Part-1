# OpenCL-path-tracing-tutorial-3-Part-1
Creating an OpenGL viewport (fixed camera)

Compiling instructions (for Visual Studio on Windows)

To compile this code, it's recommended to download and install the AMD App SDK (this works for systems with GPUs or CPUs from AMD, Nvidia and Intel, even if your system doesn't have an AMD CPU or GPU installed) since Nvidia's OpenCL implementation is no longer up-to-date.

- Start an empty Console project in Visual Studio (any recent version should work, including Express and Community) and set to Release mode
    
- Add the SDK include path to the "Additional Include Directories" (e.g. "C:\Program Files (x86)\AMD APP SDK\2.9-1\include")
    
- In Linker > Input, add "opencl.lib" and "glew32.lib" to "Additional Dependencies" 
 
- In Linker > Input add the OpenCL/OpenGL library path to "Additional Library Directories" (e.g. "C:\Program Files (x86)\AMD APP SDK\2.9-1\lib\x86")

- Disable SAFESEH in Linker > Advanced (set "Image has safe exception handlers" to NO), this is required in order to use the GLEW library which is often built with an older version of Visual Studio
    
- Add all the files to the project (or create a new file and paste the code) and build the code


For more details, see https://raytracey.blogspot.com/2017/01/opencl-path-tracing-tutorial-3-opengl.html

For part 2 of this tutorial, see https://github.com/straaljager/OpenCL-path-tracing-tutorial-3-Part-2

Screenshot:

![Image description](https://github.com/straaljager/OpenCL-path-tracing-tutorial-3-Part-1/blob/master/opencl_tut3_3.png)
