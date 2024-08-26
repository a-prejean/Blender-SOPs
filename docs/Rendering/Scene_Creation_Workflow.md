---
hide:
  - tags
tags:
  - Lighting
  - Rendering
  - Nodes
  - Learning Lunch
---

# **Scene Creation Workflow**


1. [Generate Random Environments](#1-generate-random-environments)

- [Experiment with Different Camera Positions](#2-experiment-with-different-camera-positions)

- [Quickly Light with HDRIs](#3-quickly-light-with-hdris)

- [Add Product Models](#4-add-product-models)

- [Fine-tune Placement of Objects](#5-fine-tune-placement-of-objects)

- [Extra Lighting and Polish](#6-extra-lighting-and-polish)

<!-- - [Rendering](#7-rendering) -->


!!! DIVIDER ""


## **Starting with a Completely Empty Scene**

*Open the .blend file:* ***0_Empty_Startup_Scene****.blend*

- This .blend file already has Render Settings at a good starting point.


!!! DIVIDER ""


## 1. ***Generate Random Environments***

---

### **Geometry Nodes for Environment Creation**

*Append (Reuse Data) Geometry Node Asset(s) from:* ***My_Library > Props > Scene***


#### Procedural_Geometry_Stack_Recursive
- Randomly create instances of *Procedural_Geometry_Stack* on a recursive grid


#### Recursive_Subdivision_Greeble


#### Random_Instance_Repeat_Zone


#### Triangulated_Grid


---

#### **Convert Geometry Node Results to New Geometry**
1. Adjust Settings on GeometryNodes modifier to get desired results
- Duplicate Object
- Apply GeometryNodes modifier
    - May need to delete empty material slot in Material Properties


!!! DIVIDER ""


## 2. ***Experiment with Different Camera Positions***

---

### **Camera Setup**

*Append Collection from:* ***Camera_Random_Position****.blend*

1. **Camera_Area** : *Translate* and *Scale* to define area that camera is confined

    !!! danger "Do *NOT* apply *ANY* transforms"

- **Camera_Target** : Positioned per shot
    - **DoF_Target** : Further offset as needed per shot

- **Camera_Position** : Adjust *Modifier Properties* to move camera to random location within *Camera_Area*
    - **Position Seed** : Move camera to new random location
    - **Position Offset** : Further offset camera position as needed

- **Camera_GN.00X** : Parented under *Camera_Position*
    - Track To Constrained to *Camera_Target*


---

#### **Save Camera Positions at a Particular** ***Position Seed***

{==

Use this to have multiple cameras, each at a different angle, all aiming at ***Camera_Target***

==}

1. Select ***Camera_GN.00X***
- Duplicate the camera ( ++shift+d++ then ++right-button++ click )
- ++alt+p++ then ***Clear (Parent) and Keep Transformation***
- Move to Collection ( ++m++ ) Scene Collection

!!! note "To Freely Rotate Camera"
    - Delete Track To constraint
    - Can rotate camera now, freely with camera selected, or around selected object


!!! DIVIDER ""


## 3. ***Quickly Light with HDRIs***

---

!!! note ""
    See [Notes](../Rendering/HDRI_Lighting.html) in Rendering SOP for more information, tips, and techniques

**HDRI Lighting**

- Adjust rotation and intensity for different effects

**Easy HDRI**

- See [Notes in Rendering SOP](../Rendering/HDRI_Lighting.html#easy-hdri)


!!! DIVIDER ""


## 4. ***Add Product Models***

---

!!! note ""
    See [Notes](../Rendering/Scene_Composition.html#placing-objects) in Rendering SOP for more information, tips, and techniques

**Rapid Placement in Camera View**

**Randomly distribute products as a starting point**


!!! DIVIDER ""


## 5. ***Fine-tune Placement of Objects***

---

*Split each prop and product model into individual objects for fine tuning positions*

1. Select Object and Move to New Collection ( ++m++ ) with same name as Object
- Switch to Edit mode ( ++tab++ ) and Select All ( ++a++ ) Faces
- Separate ( ++p++ ) > By Loose Parts
    - Creates one object for every independent/disconnected fragment of the original mesh.
    - All New objects should be in current Collection
- Switch to Object mode ( ++tab++ )
- *Object > Set Origin >* ***Origin to Geometry*** on all new objects
- Adjust as needed
    - Mainly from top view to avoid moving through ground plane


!!! DIVIDER ""


## 6. ***Extra Lighting and Polish***

---

Add extra lights as needed.

- [Three Point Lighting](../Rendering/Three_Point_Lighting.html)
- [Reverse Key Lighting](../Rendering/Three_Point_Lighting.html#reverse-key-lighting)
- Light_Volume_Cube
- GOBO_Light_Area


[**Light Linking**](../Rendering/Lighting.html#light-linking-cycles-only) (Cycles Only)


**Gaffer**?


**placeReflection_blender**


<!-- !!! DIVIDER ""


## 7. ***Rendering***

---

EEVEE? -->


---
