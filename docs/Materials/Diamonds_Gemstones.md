---
hide:
  - tags
tags:
  - Materials
  - Nodes
---

# **Diamonds & Gemstones**

<figure markdown="span">
  ![C_Diamond](../media/C_Diamond.png){ width="800" }
  <figcaption><em><strong>C_Diamond</strong></em> material</figcaption>
</figure>


!!! note
    Gemstone Materials can also be organized into Node Groups


## **C_Gemstone_Setup**
The original shader setup for most Gemstone materials created for catalog beauty shot renders.

<figure markdown="span">
  ![C_Gemstone_Setup_MNG_detail](../media/C_Gemstone_Setup_MNG_detail.png){ width="800" }
  <figcaption>Contents of <em><strong>C_Gemstone_Setup_MNG</strong></em></figcaption>
</figure>


- This Node Group can be used as a starting point for most Gemstone types.
- Base Color, Roughness, Index of Refraction (IOR), and Dispersion values should be all that’s needed to make almost any Gemstone material.
    - As previously mentioned, these attributes can be defined in a single node group.

<figure markdown="span">
  ![C_Gemstone_Setup_MNG](../media/C_Gemstone_Setup_MNG.png){ width="800" }
  <figcaption><em><strong>C_Gemstone_Setup_MNG</strong></em> Node Group using the <em><strong>Diamond_Attributes</strong></em> Node Group as input</figcaption>
</figure>


!!! DIVIDER ""


## **JCF Fancy Glass**
Alternative shader setup that can also be used for beauty shot renders.

- Similar to C_Gemstone_Setup_MNG, this Node Group can be used as a starting point for most Gemstone types.

<figure markdown="span">
  ![Image_Title](../media/JCF_Fancy_Glass.png){ width="600" }
</figure>

---

### **Recommended Render Settings for JCF Fancy Glass**

<figure markdown="span">
  ![Image_Title](../media/JCF_Fancy_Glass_Render_Settings.png){ width="600" }
</figure>

- **Max Samples** : At least 1024
- **Noise Threshold** : 0.001 for preview, around 0.00025 for final
- **Indirect Light** : 250 for low samples, up to around 1000 for high samples


!!! DIVIDER ""


## **Increasing Brightness**

<figure markdown="span">
  ![Increasing_Brightness_Shader](../media/Increasing_Brightness_Shader.png){ width="600" }
  <figcaption>Added Material Nodes</figcaption>
</figure>


<div class="grid" markdown>

<figure markdown="span">
  ![Increasing_Brightness](../media/Increasing_Brightness.gif){ width="400" }
</figure>

- Plug a shader's output into *BOTH* inputs of an ***Add Shader***
- Plug that output into a ***Mix Shader*** to adjust the amount of extra brightness.

</div>


---
