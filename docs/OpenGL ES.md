# OpenGL ES
The Zune HD supports the OpenGL ES 2.0 standard, which is basically OpenGL 2.0 but with a programmable render pipeline.

## Getting Started
All you have to do in order to initialize OpenGL in your application is to include ``zdkgl.h`` and call ``ZDKGL_Initialize()`` on startup. Make sure to call ``ZDKGL_Cleanup()`` before exeting. 
Sourround your render code with ``ZDKGL_BeginDraw()`` and ``ZDKGL_EndDraw()`` and you are good to go.

## Extensions
The Zune HD also supports the following extensions. 
``GL_OES_rgb8_rgba8``, ``GL_OES_fbo_render_mipmap``, ``GL_NV_depth_nonlinear``, ``GL_NV_draw_path``, ``GL_OES_EGL_image``, ``GL_OES_vertex_half_float``, ``GL_NV_framebuffer_vertex_attrib_array``, ``GL_NV_coverage_sample``, ``GL_OES_mapbuffer``, ``GL_ARB_draw_buffers``, ``GL_ARB_half_float_pixel``, ``GL_EXT_Cg_shader``, ``GL_EXT_packed_float``, ``GL_OES_texture_half_float``, ``GL_OES_texture_float``, ``GL_EXT_texture_array``, ``GL_OES_compressed_ETC1_RGB8_texture``, ``GL_EXT_texture_compression_latc``, ``GL_EXT_texture_compression_s3tc``, ``GL_EXT_texture_filter_anisotropic`` ``GL_NV_get_tex_image``, ``GL_NV_read_buffer``, ``GL_NV_shader_framebuffer_fetch``, ``GL_ARB_texture_rectangle``, ``GL_NV_fbo_color_attachments``, ``GL_EXT_bgra``