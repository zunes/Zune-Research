
# How Apps Work
Also of note is how applications function. The leaked WP7 docs note that each app runs in its own “isolated sandbox”. This is how the Zune HD functions as well. Each application is packaged into a “zcp” file which (as someone else in this thread said) seems to be some sort of almost VHD file format. Then when the app loads, it basically mounts that ZCP file and everything runs within that (zctfs.dll). The app is only allowed to read/write to that file. Although it doesn’t seem like XNA game studio apps get packaged into this (unless the Zune builds a new file and packages everything?).

# .ZCP Files
  
a) .zcp files have nothing to do with Zortech, even though they apparently have the same file extension.  
b) A .zcp file is like a mini-filesystem that can be mounted and accessed on the Zune. They're kinda like .iso images, but writable as well.  
c) Everything in XNA is stored in containers. There's 3 types of containers: game containers, runtime containers, and storage containers. All three are stored on the Zune itself as .zcp files.  
d) Runtime containers include the XNA runtime files and are identified by a particular runtime token.  
e) Game containers store everything deployed along with a game and specify the runtime container needed by the game, which is automatically loaded when the game is started.  
f) Storage containers are what games use for storing data, and have to be manually loaded through code in the game.  
g) The built-in Zune games are both signed and encrypted, making them near-impossible to modify and difficult to even analyze.  
h) The integrated runtime, which is deployed along with the games, is not encrypted, but it is signed. It isn't much different from the ordinary runtime that's deployed automatically along with user-created Zune games.  
i) The built-in games and integrated runtime are not deployed through the same method that user-created games are: they're dumped straight onto the Zune.

# Dump Rom
When you dump the ROM, make sure you use do it like this: dumprom.exe -d dump -v -5 nk.nb0

1. viewbin.exe nk.bin  
	(write down start and length)  
  
	1. cvrtbin -r -a START -w 32 -l LENGTH nk.bin  
	2. this command converts the nk.bin to a nk.nb0 (START and LENGTH from the command bevor)  
  
3. dumprom.exe -d dump -v -5 nk.nb0  
	the content of the nk.bin will be written in the directory "dump". It must exists, otherwise an error occurs.  
  
4. now, see files that is extracted and you will know that they are changed to MIPS files.

# OpenZDK
Open ZDK reverse engineered the DLLS like zdksystem.dll in order to use Zunes functionality


# OpenGL ES Extensions

``GL_OES_rgb8_rgba8``, ``GL_OES_fbo_render_mipmap``, ``GL_NV_depth_nonlinear``, ``GL_NV_draw_path``, ``GL_OES_EGL_image``, ``GL_OES_vertex_half_float``, ``GL_NV_framebuffer_vertex_attrib_array``, ``GL_NV_coverage_sample``, ``GL_OES_mapbuffer``, ``GL_ARB_draw_buffers``, ``GL_ARB_half_float_pixel``, ``GL_EXT_Cg_shader``, ``GL_EXT_packed_float``, ``GL_OES_texture_half_float``, ``GL_OES_texture_float``, ``GL_EXT_texture_array``, ``GL_OES_compressed_ETC1_RGB8_texture``, ``GL_EXT_texture_compression_latc``, ``GL_EXT_texture_compression_s3tc``, ``GL_EXT_texture_filter_anisotropic`` ``GL_NV_get_tex_image``, ``GL_NV_read_buffer``, ``GL_NV_shader_framebuffer_fetch``, ``GL_ARB_texture_rectangle``, ``GL_NV_fbo_color_attachments``, ``GL_EXT_bgra``

## CE 6.0 Docs
https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee504812(v=winembedded.60)?redirectedfrom=MSDN

https://docs.microsoft.com/en-us/previous-versions/windows/embedded/bb643806(v=msdn.10)?redirectedfrom=MSDN

https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee483032(v=winembedded.60)

https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee482973(v%3dwinembedded.60)

https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee488372(v%3dwinembedded.60)