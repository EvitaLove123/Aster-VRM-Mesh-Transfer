# Aster-VRM-Mesh-Transfer

Browser-based VRM/GLB mesh transfer workshop, designed for mobile browsers and GitHub Pages.

## Current early build
- Import a target (A) and source (B) model in VRM or GLB format.
- Preview the target in a Three.js viewport.
- Browse source and target meshes; identify static vs skinned meshes.
- Add or replace **static** meshes.
- Move, rotate and scale selected target meshes using Three.js TransformControls or numeric inputs.
- Export the current target scene as GLB.

## Important limitations
This is an early static-mesh prototype, not a complete VRM editor.
- Skinned meshes are detected but transfer is blocked until correct skeleton remapping, skin weights and inverse bind matrices are implemented.
- Full Skeleton Merge, Humanoid remapping, Spring Bones, colliders, VRM expressions and VRM 0.x/1.0 export are not implemented yet.
- GLB export is not VRM export.
- Dependencies are loaded from a CDN; an internet connection is required. Model files are processed locally in the browser and are not uploaded to a server.

## Run on GitHub Pages
1. Open **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main`, folder `/ (root)`, then Save.
4. Open the published Pages URL after deployment completes.

## Technology
- Three.js
- Three.js GLTFLoader, GLTFExporter, OrbitControls, TransformControls
- @pixiv/three-vrm loader plugin (loading only; no UniVRM)
