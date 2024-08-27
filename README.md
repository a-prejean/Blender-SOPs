# Blender-SOPs
SOPs for Creating 3D Renders with Blender


*Both instances should always match since they're created from the same source.*


## Auto Build GitHub Pages
- Changes made in ***root/docs/*** will be reflected in https://a-prejean.github.io/Blender-SOPs/index.html once committed


## Saving Static Site to Server
- Use ***mkdocs build*** and copy contents of created ***site*** folder to server


---


# Links
https://chrisbrejon.com/cg-cinematography/
https://magic-mark.com/how-to-create-caustics-in-blender/
https://www.blendernation.com/2024/01/13/5-lighting-tips-for-blender/

# Photography References
https://expertphotography.com/the-complete-guide-to-photography-composition-78-tips/
https://expertphotography.com/golden-ratio-photography/
https://expertphotography.com/golden-ratio-vs-rule-of-thirds/
https://expertphotography.com/golden-triangle/
https://expertphotography.com/improve-your-composition-the-rule-of-thirds/
https://expertphotography.com/composition-visual-weight-influence-viewers/
https://expertphotography.com/20-tips-shallow-depth-of-field/


---


# Examples
i.e., ("that is")
e.g., (“for example”)


# Getting Started

Open Terminal
pip install mkdocs-material
  or, pip install --upgrade mkdocs-material

In Project Directory, in terminal:
mkdocs new .

pip install mkdocs-glightbox
  or, pip install --upgrade mkdocs-glightbox
  If getting no such file or directory, try
  pip3 install --upgrade pip
pip install --upgrade pip


# Previewing as you write
mkdocs serve
OR
mkdocs serve --dirtyreload
    for current page only

Point your browser to http://localhost:8000/


# Building your site
mkdocs build


If you intend to distribute your documentation as a set of files to be read from a local filesystem rather than a web server (such as in a .zip file)


# Building for offline usage
Add the following lines to mkdocs.yml:
plugins:
  - offline

### Limitations
All features that use the fetch API will error.
Disable the following configuration settings:
- instant loading
- site analytics
- git repository
- versioning
- comment systems


# Customization
In order to make a few small tweaks to Material for MkDocs, you can just add CSS and JavaScript files to the docs directory.
https://squidfunk.github.io/mkdocs-material/customization/



# Formatting
*Italic*
**Bold**
***Bold_Italic***
==Highlighted==
***==Highlighted_Bold_Italic==***


{==

Highlighted_Text_Block

==}


keyboard keys: ++ctrl+alt+del++



# Images

https://squidfunk.github.io/mkdocs-material/reference/images/

![Image_Title](../media/Image.png){ width="800" }

<!-- Image Left or Right Aligned -->
![Image_Title](../media/Image.png){ align=left }

<!-- Image Centered -->
<figure markdown="span">
  ![Image_Title](../media/Image.png){ width="600" }
</figure>

<!-- Image with Caption -->
<figure markdown="span">
  ![Image_Title](../media/Image.png){ width="600" }
  <figcaption>Image_Caption</figcaption>
</figure>



<!-- Text on Left with Image on Right -->
<div class="grid" markdown>

- TEXT

![Image_Title](../media/Image.png){ width="340", align=right }

</div>

<!-- use div to organize grid items -->
<div></div>
<!-- or -->
<div markdown>

</div>



# Navigation
Pages will show up in order listed in mkdocs.yml:

nav:
  - index.md
  - page.md



# Grid Layouts

<div class="grid" markdown>

Some Text

![Image_Title](../media/Image.png){ width="340", align=right }

</div>



# Callouts / Admonitions
!!! note
    TEXT

???+ note
    TEXT

!!! note ""
    TEXT



# Dividers
!!! DIVIDER ""






# Mentioning Appending Assets

*Append AssetType from:* ***AssetName****.blend*

AssetType:
Collection
Object
Geometry Node Group
World




---


# Future Additions

---

- https://www.blendernation.com/2024/06/24/get-better-lighting-in-blender-with-this-easy-trick/


## **IES Lights**
  - https://www.youtube.com/watch?v=7yTTbpY1jXQ

#### **Starting Point Settings:**

##### IES_Display

- Power: 0.5 W
- Similar to IES_3LobeVee

##### IES_3LobeUmbrella

- Power: 6 W

##### IES_DefinedSpot

- Power: 1.825 W
- Similar to IES_DefinedDiffuseSpot, IES_3LobeUmbrella


#### **Simple Lights:**

!!! note
    *ALL based on Power: 10 W, Radius: 1 m, Distance from origin: 1 m*

| Texture | Strength |
| --- | --- |
| area-light.ies | 0.025 |
| comet.ies | 0.025 |
| defined.ies | 0.03 |
| jelly-fish.ies | 0.1 |
| overhead.ies | 0.015 |
| umbrella.ies | 0.04 |
| x-arrow-diffuse.ies | 0.75 |


#### **Detailed Lights:**

!!! note
    *ALL based on Power: 10 W, Radius: 1 m, Distance from origin: 1 m*

| Texture | Strength |
| --- | --- |
| bollard.ies | 0.3 |
| defined-diffuse.ies | 0.25 |
| defined-diffuse-spot.ies | 0.5 |
| defined-spot.ies | 0.175 |
| display.ies | 0.125 |
| medium-scatter.ies | 1.0 |
| scatter-light.ies | 0.045 |
| three-lobe-umbrella.ies | 0.4 |
| three-lobe-vee.ies | 0.1 |
| trapezoid.ies | 0.035 |
| vee.ies | 0.4 |
| x-arrow.ies | 1.25 |
| x-arrow-soft.ies | 3.0 |


---

# Prop and Surface Materials
(Props_Surfaces_Materials.blend)

---

## Reflectors and Diffusers:
These can help control the lighting and prevent unwanted reflections on the jewelry. Reflectors bounce light onto the subject, while diffusers soften and disperse it.

### **GEO Lights**

#### LightDiffuser

- Rotate similar to light source
- Further from light the more diffused

---

## Render EACH ring alone and comp them all together? (Compositing)

---

## GeoNodes

---

# Chains
(see Notion, https://www.notion.so/Chains-5bf28fbe8c704283bc76fc772dafaa10)

---

# Resolutions
Full Spread: 17 x 11 inches @ 300dpi = 5100 x 3300
Page: 8.5 x 11 inches @ 300dpi = 2550 x 3300
4K reference resolution = 4096 × 3072 pixels (4:3)
8K = 8192 x 6144 (4:3)


# Test Render sizes:
- 4800 x 4000
- 2400 x 2000
- 1200 x 1000

---

# **Saving:**
Image Viewer (Render Result) > Image > Save As (0% Compression)

---

# Python scripts to Render Specific Collections with specific HDRIs

---

# Fast GI Approximation: Enabled???
- Viewport Bounces: 4-32 (higher for more “brilliant” diamonds)
- Render Bounces: 4-32 (higher for more “brilliant” diamonds) 1024?

---

# View Layer Properties

---

# Light Path node
- Ray Depth

---

# Light Groups
- Object Properties > Shading > Light Group

---

## Blender 4.0 Lighting

### Path Guiding

### Energy Conservation

---

# Lessons from Traditional Photography
- you need a specular light source, with some fill (both white line and some black line fill)

- You will see the sparkle best when the stone is displayed against a black background, which is why black velvet is used.

- One of the four Cs for diamonds is Cut (the other are Color, Clarity, Carat wt.) Cut has more to do with the value of a stone than diameter or weight on the because if the stone is cut too shallow or too deep the light does not refract off the facets very well and will lack the "fire" a diamond is famous for. 
- That's why you don't go to the jeweler and ask for a 4mm diamond, like you would pearls. You ask for a weight range and color range, then check the cut and sparkle and the inclusions. 
- Big diamonds are cut around the inclusions. A window will be polished into a rough stone and the cutter will study the internal structure before planning how to cut and polish it so any imperfections called inclusions (carbon specks or other minerals) will be not be visible when the stone is view -- they can be hidden in the refraction. Color and clarity are graded and easy for a neophyte to understand. Cut isn't graded and is where the unsophisticated shopper can be mislead. Some stones are intentionally cut shallow because a shallow cut will produce a bigger looking stone than a properly cut stone of the same wt.

- Try starting with one point source like a small halogen desk lamp ( not a long worklight bulb ) or a bare strobe on black velvet and compare it with other things you've tried.


---


# Compositing Nodes


## **Final Image Node Hierarchy**

<!-- Image with Caption -->
<figure markdown="span">
  ![Image_Title](./media/Image.png){ width="600" }
  <figcaption>Image_Caption</figcaption>
</figure>

Render Layers > Despeckle? > Tonemap? > Glare > Color Mix (Add) > Color Balance > Composite


## Troubleshooting
- Timing Overlays
    - See the impact of nodes added


### Bloom (Cycles / EEVEE)
- Handled through Compositing tab
- Viewport Shading dropdown (while in Rendered mode)


---


# Separate a Single Mesh by Materials
Select Object
Switch to Edit mode (Tab)
Select All (A)
P > By Material
Materials will need to be reapplied


---


- Try Noise Texture to generate random shapes instead of recursive subdivision?
- if you find the normal you can do a kind of marching cubes thing using different lego bricks?


---


- Select ***Procedural_Collection_Object_Repeat*** object
- *Modifier Properties > GeometryNodes*
    - For *Collection* select  ***PRODUCT_MODELS***
- Adjust Settings on GeometryNodes modifier to get desired results
- Duplicate Object
- Apply GeometryNodes modifier
    - Materials for all objects instanced should still be applied


---
