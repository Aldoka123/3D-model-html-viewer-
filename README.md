# 3D-model-html-viewer-
Browser-based 3D character viewer and pose editor. Load GLB, GLTF, FBX, VRM, OBJ, DAE, STL, PLY or 3DS models, pose bones, drive face morph targets, play animations and keyframe poses. Single HTML file, fully client-side.
Character Studio is a single-file, fully client-side web app for inspecting and posing 3D characters. Drop a model into the browser and control its body, face and animations in real time. Nothing is uploaded to a server.

Features

Formats: GLB, GLTF (with .bin and textures), FBX, VRM 0.x, OBJ (+MTL), DAE, STL, PLY, 3DS.
Viewer: orbit, zoom and pan, perspective or orthographic camera, grid, lighting and shadows, background color, fullscreen.
Pose editing: click a joint on the model or pick a body part from the list, then rotate it with a Blender-style gizmo or sliders. Covers head, neck, arms, hands, spine, chest, hips and legs.
Face controls detected from the model itself: morph targets, VRM expressions and face bones (jaw, eyes) are scanned from the loaded file, not assumed from its format. Quick controls for mouth, smile, blink, gaze and brows appear only when the model has them. A searchable list shows every shape.
Animations: lists clips found in the file, with play, pause, stop, loop and speed.
Presets and poses: built-in poses and expressions, plus save, load, reset and export of poses as JSON (bone rotations and blend shape values).
Timeline: add or delete keyframes, with smooth interpolation between poses and looping.
Graceful fallbacks: controls for missing skeletons, morphs or animations are disabled, and unsupported files show a clear error.

Tech: vanilla JavaScript, Three.js r128 (loaders, OrbitControls, TransformControls), @pixiv/three-vrm 0.6. No build step, just open index.html.

Known limitations

VRM 1.0 files load as plain GLB, without expressions.
Built-in pose presets assume a T-pose rig.
Skeleton sliders are disabled while a clip from the file is playing.
Suggested usage section
# Run locally
Open index.html in any modern browser (or serve with `npx serve .`).
Drag and drop a model onto the left panel, or click Upload Model.


