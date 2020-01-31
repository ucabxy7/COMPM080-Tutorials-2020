# Coursework 1 F&Q list


1. loading PLY: you can also use igl::readPLY and writePLY.


2. sub-sampling step in ICP: we suggest you start with non-subsampling step (use all input points if your machine allows). After your implementation looks work, you can try sub-sampling and answer item `4. Instead of directly aligning...` 

3. rejection step in ICP: a simple one is to check normal vectors' angle

4. visualization: you can also use MeshLab to create some result screenshots. 

5. can I just visualize 'points' instead of meshes ? : ok -- make sure we can understand your alignment results and also see the normal information through point color (question 6)

6. what is `adjusting the noise to the bounding box...` 
Give a point set, its bounding box can be defined by the maximum and the minimum coordinates. This step is used to add meaningful noises since the coordinate of a mesh is not always aligned with the real world metric (so 0.1 in M2's space can be 0.1 cm/0.1 meters or 0.1 X depends on how M2 is created) 

7. what is normal shading:
Normal shading : points colored based on their normals being mapped to rgb. It can be changing vertices color using normal vectors. 
e.g.
![Image](/course_work_1/imgs/nv_shading.png)  


## Results reference

**bun045.ply TO bun000.ply**  
no noise/no subsampling/no rejection/point2point  
![Image](/course_work_1/imgs/45_to_00.gif)
![Image](/course_work_1/imgs/45_to_00_fin.jpg) 
![Image](/course_work_1/imgs/45_to_00_err.jpg)  


**bun090.ply TO bun000.ply**  
no noise/no subsampling/no rejection/point2point  
![Image](/course_work_1/imgs/90_to_00.gif)
![Image](/course_work_1/imgs/90_to_00_fin.jpg) 
![Image](/course_work_1/imgs/90_to_00_err.jpg)
