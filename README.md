
Maya CgFX Shaders
====

Simple NPR shader demos in Maya.
This package includes the following NPR techniques.

* **Lit-Sphere** [Sloan et al. 2001]
    - View-dependent texture map to capture artistic shading styles.
* **X-Toon** [Barla et al. 2006]
    - Extension of cartoon shader for providing additional shading behavior with a 2D texture.

## Result
### Lit-Sphere
![Lit-Sphere](LitSphere/results/LitSphere.png)

### X-Toon
![X-Toon](XToon/results/XToon.png)

## Usage
### Directory Structure
* [ShaderName]
    - cgfx: CgFX shader files.
        - [ShaderName].cgfx: main CgFX shader file.
        - builtInMatrix.cgh: Maya built in matrix declaration.
    - sourceimages: sample texture files for the shader.

### Maya
You can use these CgFX shaders (**LitSphere.cgfx** or **XToon.cgfx**) from a built-in Maya CgFXShader material node.

1. Load the CgFX shader plug-in.
    * Window > Settings/Preferences > **Plug-In Manager**
    * In the Plug-In Manager, Load the **cgfxShader.mll** plug-in.
2. Create a CgFX shader material.
    * Right-click the target object and select **Assign New Material**.
    * In Assign New Material window, select the **CgFX Shader material** from the Maya > Surface list.
    * The CgFXShader material node appears in the Attribute Editor.
3. Load the target CgFX shader file (**LitSphere.cgfx** or **XToon.cgfx**).
    * From the CgFX File attribute, you can load the .cgfx file you want to use.
    * The CgFX shader plug-in automatically loads shader attributes.

#### Shader Attributes
##### Lit-Sphere shader attributes.

|Attribute  |Description    |
|-----------|---------------|
|colorSampler (Color Map)|  Texture attribute for the Lit-Sphere shader.<br/> - **sourceimages/LitSphereTexture.png** can be used for testing. |

##### X-Toon shader attributes.

|Attribute  |Description    |
|-----------|---------------|
|Light Position  |Point light location for the illumination.    |
|XToonSampler (XToon Map)|  Texture attribute for the X-Toon shader.<br/> - **sourceimages/XToonSilhouette.png** can be used for silhouette effect.<br/> - **sourceimages/XToonSpecular.png** can be used for specular effect.   |
|Show Diffuse  |Show diffuse shading term.    |
|Show Specular  |Show specular shading term.    |
|Show Silhouette  |Show silhouette term.    |
|Silhouette Effect  | 0: 2D texture is used for specular effect.<br/> 1: 2D texture is used for silhouette effect.   |


## License

The MIT License 2015 (c) tody