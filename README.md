# Vansan

Stylized, seamless PBR material collections for game environments.
Published on the Unity Asset Store under the publisher name **Vansan**.

This repository is the public portfolio linked from that publisher profile.
It shows the work. It does not distribute it.

## What this is

Four collections, 30 materials each, built as tileable 2K texture sets for
stylized games: villages, starship interiors, dungeons and sunlit courtyards.
They share one visual language so they can be used together.

| Collection | Materials | Subject |
|---|---:|---|
| Fantasy Village Ground | 30 | Cobblestone, meadow grass, dirt roads, plazas, biome floors |
| Sci-Fi Panels + Emissive | 30 | Hull panels, circuit floors, metal decks, grates, hazard marking |
| Fantasy Dungeon | 30 | Flagstone, mossy brick, lava, ice, dark iron, set-piece floors |
| Light Stone + Moss | 30 | Limestone, marble and pale flagstone with moss in the joints |

## What every material includes

Eight maps at 2048 × 2048, PNG, lossless:

- Albedo
- Normal, OpenGL convention
- Roughness
- Metalness
- Height
- Ambient Occlusion
- HDRP Mask Map — R metalness, G ambient occlusion, B detail mask, A smoothness
- ORM pack for Godot

Unity packages add a `Universal Render Pipeline/Lit` material per texture set,
a demo scene and an offline setup guide in PDF and RTF. The same PNG maps work
in Unreal Engine, Godot and Blender. DirectX workflows need the normal map's
green channel flipped.

Glow materials in the sci-fi and dungeon sets also include an emissive mask.

## How the textures are made

Albedo base textures were generated locally using Stable Diffusion XL
(commercial license) in ComfyUI. All generated outputs were curated,
seam-repaired (inpainting and edge matching for seamless tiling), upscaled to
2048×2048, and processed with procedurally derived PBR maps (Height, Sobel
Normals, Roughness, Metalness, and Ambient Occlusion). No third-party
copyrighted materials were used as source inputs.

The pipeline, in order:

1. Generate albedo candidates locally.
2. Curate. Outputs with a broken read, or that resemble existing work, are
   discarded.
3. Repair seams with inpainting and edge matching, then check tiling on both
   axes.
4. Derive the remaining PBR maps procedurally and upscale to 2K.
5. Build the Unity material, mask map and ORM pack from those maps.

## About the images in this repository

The JPEGs under `images/` are reduced previews, exported at 512 px from the
albedo of the **free sample** of each collection. They exist so the work can
be seen. They are not the product.

- They are not the 2K source files.
- They are not a license to use the textures in a project.
- They do not include normal, roughness, metalness, height or occlusion maps.

The paid collections are not published here at all, not even as previews.
Full-resolution maps, the complete map set and the Unity materials are
distributed only through the Unity Asset Store, under the Asset Store EULA.

A free five-material sample of Fantasy Village Ground is available on the
Asset Store for evaluation before buying.

## Compatibility

- Unity 6, Universal Render Pipeline. Tested in 6000.3.25f1.
- Built-in is supported through included MetallicSmooth helper maps.
- HDRP through the included Mask Map.
- Unreal Engine, Godot and Blender through the raw PNG maps.

## License

Source textures, materials and preview images are not licensed for reuse by
this repository. See the Asset Store listing for the applicable EULA.

## Contact

Unity Asset Store, publisher **Vansan**.
