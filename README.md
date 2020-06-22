GENERAL INFO

	This project's goal is to experiment around with raytracing octrees, as well as octrees in general.
	
	It is currently focused around a compressed, yet dynamic octree-implementation, which can be found
	in och_h_octree.h.
	
	The ray-traversal algorithm is an adapted version of the one presented by Samuli Laine and Tero 
	Karras in the appendix of Efficient Sparse Voxel Octrees: Analysis, Extensions, and Implementation
	(Nvidia Research, 2010).
	I recommend having a look at the original paper to gain an understanding of the algorithm, as this
	one is a bit lacking when it comes to comments.
	The major adaptations are the use of a bitmask indicating the dimension of the currently traversed
	node, as well as an early branch which avoids an overstep-correction when traversing up the tree.

GETTING IT RUNNING

	The easiest way of executing the code on your own machine is using Visual Studio and its Git/Github
	integration. If you aren't familiar with this extension I recommend Bill Raymond's Video "Up and 
	Running with GitHub and Visual Studio 2019" (https://www.youtube.com/watch?v=csgO95sbSfA).
	From there it should be a simple matter of compiling the solution and... voila.

KEYBINDS

	Camera movement:

	W, A, S, D		Move camera
	C				Switch camera-mode between horizontal and directional movement
	Shift			When the camera is in horizontal move-mode, move down
	Space			When the camera is in horizontal move-mode, move up
	Mousewheel		Change camera-speed. If Shift is pressed as well, change slower

	Interaction with tree:

	LMB				Remove a voxel
	RMB				Place a new voxel
	T				Place 40^3 voxels
	Z				Remove 40^3 voxels

	Various:

	ENTER/ESC		Close window
	I				If the camera is in an active voxel, move it to the first empty voxel above it
	O				Toggle debug-output in top right of screen
	M				Mark a point to measure a distance

	These are only available when the Visualisation-window is open and in focus.

CUSTOMIZATION

	Customization comes in two varieties: First off, voxels and their colours can be specified in the file
	"voxels.txt". Secondly, the generated terrain can be defined in "terrain.txt". (This is
	not implemented yet).