-- Fixed Layer Width Script --
-- By Jasper Cohen --
-- 2/19/2024--

This script turns polysurface files (imported okay) into solid relative thickness meshes which can then be sliced into consistent single or multi-perimeter line prints. this scirpt is a workaround for slicers that lack this inate cabaility like orca or slic3r. Cura allows for single wall mesh printing when in 'Surface Mode'. 

The script does this through the following steps:
1). convert polysurface to mesh
2). thicken mesh
3). point move offset surfaces to achieve uniform thickness at local elevation xy plane.

For best results consider the following:
1). use fillets in your polysurface. sharp corners confuse the thickening operation in some instances. sharp corners are also more likely to create a break in the slicer result. 

This script is very much a workaround. The better way to make a single line print would be to program the toolpath itself. but, that would also involve sending custom gcode, which always carries the risk of damaging an otherwise functional printer. consider this script for the not so brave of heart. 

Dependencies:
1). [The Pufferfish Grasshopper plugin]([url](https://www.food4rhino.com/en/app/pufferfish)https://www.food4rhino.com/en/app/pufferfish)

