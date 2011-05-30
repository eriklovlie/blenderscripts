= Aim

Low threshold for getting graphics content from blender and into GLES.
No "engine" assumed (engines are dependencies).
Reduce num of required dependencies on target (fread + GLES should be enough).

= Features:
* Scene
* Camera
* Object
* Material (image only)
* Mesh
  * vertex position + normal
  * faces (smooth + solid, optionally one uv layer)

= Todo
* animation
* armature

= Howto

== Initial setup
Download prozess and put it "somewhere"
Download and install Blender 2.57 from blender.org
cd <path to blender>/2.57/scripts/addons
ln -s <path to prozess>/prozess

== Every time
Open Blender
Create some content
Open the "Scripting" perspective
In the console, write:
	from prozess import prozblend as proz
To reload script after making changes:
	from imp import reload
	reload(prozess)
To dump a scene:
	proz.dump()
