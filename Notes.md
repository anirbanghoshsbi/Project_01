**Optical Flow :** (source : wiki)

Is the pattern of apparent motion of objects , surfaces , and edges in a visual scene due to the relative motion between the scene and the observer. This concept was introduced by American Psychologist James Gibson to describe the concept visual stimulus provided to animal moving through the world.
This term is used by roboticist encompassing related techniques from image processing and control of navigation including motion detection , object segmentation , motion compensated encoding and stereo disparity measurement.

The optical flow methods try to calculate the motion between two image frames whixh are taken at times t and t + delta(t) at every  _voxel_ position.

These optical flow methods use the differential mathematics as they are considered discrete and follow Taylor series approximation. Here the partial differentiation is taken with respect of spatial co-ordinates ( co-ordinates  ) and temporal (time) co-ordinates.

For a 2-Diamensional case a voxel is located at (x , y , t) with intensity  I(x , y, t) , the voxel will be moved between the two image frames.
I (x , y, t) will be moved by delta(x) , delta(y) , delta(t) 
We now make two implicit assumption 
a) there is a brightness constancy constraint 
giving 

I(x , y , t) = I(x +delta(x) , y +delta(y) , t + delta(t))

b) there is a infinitesimal change in displacement 
I(x + delta(x), y + delta(y) , t + delta (t)) =  I ( x , y , t) + d(I)/d(x)*d(x) + d(I)/d(y)*d(y) – H.O.T

From these equations we can come up with this :
d(I)/d(x)*d(x) + d(I)/d(y)*d(y) +d(I)/d(t)*d(t) = 0
d(I)/d(x)*(d(x)/d(t)) + d(I)/d(y)*(d(y)/d(t)) + d(I)/d(t)*(d(t)*/d(t))

dI/dx*V_x + dI/dy*V_y +dI/dt =0
where V_x an d V_y are the velocity component of optical flow of I(x ,y,t) and dI/dx , dI/dy , dI/dt are the derivative of the image at (x,y,t) in the dirextion of I_x ,I_y , I_z.

Thus :

I_x*V_x + I_y*V_y  =-I_t 
This is an equation of two unknowns and cannot be solved as such.
This is called the aperture problem of the optical algorithms.

Therefore to solution for this equation can be obtained using, another set of equations, given by some additional constraints for estimating the actual flow.

Various method used for calculations :
Example lucas-Kanade , Horn-Schunck , Buxton-Buxton , etc.

Uses of optical flow :-

Motion estimation , video compression are the major aspect of optical flow research. However , the optical flow methodis also used for estimation of three-diamensional nature and structure of scene , as well as 3D motion of objects and the observer relative to the scene most of them using the image _jacobian_.

Other applications of optical flow includes :

1. object detection and tracking 
2. determining the structure of object and the environment. As the _determination of mental maps of the struture
   of our environment are critical components of animal and human vision_ , the conversion of this innate ability to a 
   computer is similarly crucial.
 
 
 ** Motion interpolation ** (source : wiki)
 
 Motion interpolation is a common, optional feature of various modern display devices such as HDTVs and video players, aimed at _increasing perceived framerate or alleviating display motion blur, a common problem on LCD flat-panel displays._

(Source : Adv Machine Learning Coursera : image analysis):-


Uses of optical flow is in video analysis.
Optical flow is : apparent flow of _pixels_ between the frames.

Deep Learning in optical Flow :
FlowNet : has twon architecture.
a) 2 images are concatenated into a single image with six channels instead of three.This image is then passed
through the convolutional neural network.
b) The siamese architecture. The two frames passed through a CNN separetely for future computation. 
