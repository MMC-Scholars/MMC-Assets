# MMC-Assets

A collection of various modelling assets used across MMC virtual reality projects. The assets are organized by categories.

## Table of Contents
1. [Notes](#notes)
2. [File Naming Conventions](#naming)

## Notes <a name="notes"></a>

- When adding assets to this repository, **make sure** that the assets have the correct permissions and are in a useable or editable format. This means removing metadata files such as `.blend1` files.

- If a texture is made from scratch, it is a good idea to save the editor file as well. This means saving `.xcf` files for [GIMP](https://www.gimp.org/) and `.psd` files for [Photoshop](https://www.adobe.com/products/photoshop).

- Save files in reuseable or lossless formats. These formats do not distort or lose quality when reproducing. The universal file type is the recommended format for saving an asset.

  File Type | Universal |  Lossless formats | Lossy formats (do not use)
  --- | --- | --- | ---
  Materials | `tga` | **`bmp`, `png`, `raw`, `tga`, `tif`** | `gif`, `jpg`, `jpeg`, `webp`
  Models | `fbx` | **`fbx`, `mtl`, `obj`** | `dae`
  Sounds | `wav` | **`flac`, `wav`** | `mp3`

## File Naming Conventions <a name="naming"></a>

In order to provide uniformity across all assets, each asset should be named in the same way to ensure assets are easy to find. The following are rules for naming assets:

- File names are self explanatory. A user should not have to open the asset to understand what the file or asset represents.
- Files are named using [lower camel case](https://en.wikipedia.org/wiki/Camel_case). That is, spaces are removed and the first letter of each word (excluding the first word) is capitalized.
- File names are as concise as possible. Instead of `dellRotatingComputerMonitorWithDisplay.jpg`, why not try `dellComputerMonitor.jpg`, or even `computerMonitor.jpg`?
- Files names are not redundant. `explosionSound.wav` can just be `explosion.wav`.
- If a file already exists with that name, append your first (and if needed, last) name to the end of the file name. For example, if `light.blend` already exists, you can instead add `lightJohn.blend` to the repository.
- Since there are many types of textures, using common naming techniques will help differentiate between texture types. _These are the only exceptions to the lower camel case naming rule_:
  Type | New Name
  --- | ---
  Ambient Occlusion | `wood_ao.tga`
  Color/Diffuse | `wood.tga`
  Displacement | `wood_d.tga`
  Glossiness | `wood_g.tga`
  Normal/Bump | `wood_n.tga`
  Roughness | `wood_r.tga`
  Specularity/Reflection | `wood_s.tga`