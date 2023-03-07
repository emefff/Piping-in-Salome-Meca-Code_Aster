# Piping-in-Salome-Meca-Code_Aster
One possibility for simulating pipes in Salome-Meca/Code_Aster.

Pipes may be simulated in Code_Aster with using special pipe elements, or jus plain 3D geometries, like we did here. Everything is done in Salome-Meca and Code Aster.

First create a path for the pipe (line element, arcs, wahtaever you need are then summarized in a 'wire'). If you want to use pipe elements, then you are basically done here. If you want to design a piping in 3D, then extrude a ring with appropriate dimensions along this path. 

This gets you a 3D geometry of you pipe. Then define appropriate groups, maybe fixations and the inner suface for the pressure. 

Mesh the part, here we used netgen with quad elements.

The displacement result below shows a piping with one end and first elbow fixed. Due to the differences of the inner surfaces on either side of the pipe, the free end wants to unfold:

![Bildschirmfoto vom 2023-03-07 08-46-40](https://user-images.githubusercontent.com/89903493/223358472-90062f9c-7799-4f18-b333-f1af676b9e80.png)
