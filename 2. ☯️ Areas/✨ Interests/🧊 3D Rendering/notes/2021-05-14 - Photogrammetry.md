[[3D Rendering]]

Source: https://www.youtube.com/watch?v=SuNNyjs9BO8

# [[Photogrammetry]]

Scanning a real world object with photos or video to generate an accurate 3D computer model.

The level of detail in the [[Photogrammetry]] scans are immense, generating millions of polygons in the 3D computer model.

## Process

### Alignment

An key factor for this technique to work is for the software to understand and camera positions given the collection of source photographs, creating a "sparse point cloud". These coordinates are then calculated to accurately stitch together the virtual surroundings of the captured object to model.

### Mesh Reconstruction

The generated model polygons are then simplified, greatly reducing the polygon count so that the models can realistically be used.

### Vertex Color Calculation

Color captured from the photo source is mapped onto the polygon vertex of the model. This is then converted and consolidated into a texture data which is applied over the mesh.

## Distortion

If the generated 3D model is distorted, there's a good chance the source photos were misaligned, inconsistent, missing data (being angles), or of poor quality.

This technique does not work well on objects that are too light, too thin, lacking detail, or is reflective.

---

Tags: [[Workflows]]

---
