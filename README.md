# MMC-Assets

A collection of various modelling assets used across MMC virtual reality projects. The assets are organized by categories.

## Table of Contents
1. [Getting Started](#intro)
2. [General Rules](#rules)
3. [File Naming Conventions](#naming)
4. [Materials](#materials)
5. [Models](#models)
6. [Sounds](#sounds)

## Getting Started <a name="intro"></a>

If your computer does not already have a local version of this repository, clone it using GitKraken.
Since there is no risk of broken code with assets, Gitflow is not used in this repository, therefore we only use the master branch for commits and production assets.
Just make sure to never push anything new before first pulling from the main repository and to follow the rules and general guidelines set in the remainder of the readme.

## General Rules <a name="rules"></a>

- When adding assets to this repository, **make sure** that the assets have the correct permissions and are in a useable or editable format. This means removing metadata files such as `.blend1` files.
- Place assets in their respective and relevant folders, starting with the three major assets: Materials, Models, and Sounds. Project-specific assets will have their own respective folders within these three categories.
- Consult other team members before creating additional folders.
- If a texture is made from scratch, it is a good idea to save the editor file as well. This means saving `.xcf` files for [GIMP](https://www.gimp.org/) and `.psd` files for [Photoshop](https://www.adobe.com/products/photoshop).
- Only save files in reuseable or lossless formats. These formats do not distort or lose quality when reproducing.

  File Type | Universal |  Lossless formats
  --- | --- | ---
  Materials | `tga` | **`bmp`, `png`, `raw`, `tga`, `tif`**
  Models | `fbx` | **`fbx`, `mtl` + `obj`**
  Sounds | `wav` | **`flac`, `wav`**

## File Naming Conventions <a name="naming"></a>

In order to provide uniformity across all assets, each asset should be named in the same way to ensure assets are easy to find. The following are rules for naming assets:

1. File names are self explanatory. A user should not have to open the asset to understand what the file or asset represents.
2. Files are named using [lower camel case](https://en.wikipedia.org/wiki/Camel_case). That is, spaces are removed and the first letter of each word (excluding the first word) is capitalized.
3. File names are as concise as possible. Instead of `dellRotatingComputerMonitorWithDisplay.png`, why not try `dellComputerMonitor.png`, or even `computerMonitor.png`?
4. Files names are not redundant. `explosionSound.wav` can just be `explosion.wav`.
5. If a file already exists with that name, append a number to the each end of the files' names. For example, if `light.blend` already exists, change it to `light01.blend` and add  `light02.blend` to the repository.
6. If a file is different enough from the numbered files, e.g `wood01.png`, append a descriptor to the end of the file name, e.g `woodBurnt01.png`.

Since there are many types of textures, using common naming techniques will help differentiate between texture types. _These are the only exceptions to the lower camel case naming rule_:

  Material | File Name
  --- | ---
  Ambient Occlusion | `wood_ao.png`
  Color/Diffuse | `wood.png`
  Glossiness | `wood_g.png`
  Macro | `wood_m.png`
  Normal/Bump | `wood_n.png`
  Roughness | `wood_r.png`
  Opacity | `wood_o.png`
  Specularity/Reflection | `wood_s.png`
  UV Layout | `wood_uv.png`

## Materials <a name="materials"></a>

The material-specific ruleset is as follows:

- Keep original textures as described in the General Rules section in the highest possible resolution. We can always downgrade on resolution with `.psd` or `.xcf` files, but not always vice versa.
- Exported texture images should always be exported as `.png`, starting out at 256x256 resolution.
- `.tga` files cannot be previewed in File Explorer like `.png` or other types. GIMP or Photoshop should be used to browse through textures. 
- If a very detailed texture is going to be used and/or the texture needs to be scaled up, then it should be exported at a higher resolution.
- All model-specific materials are never in the materials folder and should be placed with the model it is being used by. Most materials in this section are ones usually applied to surfaces such as walls or the ground.

## Models <a name="models"></a>

The model-specifc ruleset is as follows:

- When making Blender models, try to separate objects that have different textures within the model. For example, a tree should have an object for the bark and one for the leaves. The reason for this is to be able to easily apply different textures onto the same model.
- All Blender models share the same origin within the editor, which is the very center of the space. The model also should not float or be below the ground in Blender, so when it is exported to Unreal the model has the same location as other models.
- All Blender models are made with attention to real world scale, being exported at scale 100.0, Z-axis up, and X-axis forward. This is to prevent fidgeting with the scale of the model in Unreal, which should always be 1:1:1 when dragged into the gameworld.
- Models are placed in relevant folders similar to materials and sounds, but have its own folder with the same name as the model. 
- Each model folder has the `.blend` file, an exported `.fbx` file, and any of the specific materials used in texturing the model.

## Sounds <a name="sounds"></a>

The sound-specific ruleset is as follows:

- Save all sounds in `.wav` file format.