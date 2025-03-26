# KerrMicrsocopyProcessing
Labview codes for extracting hysteresis loops from Kerr images
At first, we need to align images, so that the rotation is the same.

For that, we are going to use PatterMatchAlignImagesRotation.vi.
When you run this program, it will ask you for the path to the folder of images you want to rotate. After selecting the desired folder with images you need to click to the index field and change to value from 0 to 1 to see the image. If your folder name is something like 20deg you can click on the GetRotFromFileName button to automatically get the angle of rotation. If it does not refresh the RotBy field, you need to again change the index number.

To have the same center of rotation for all angles, you must select the little cross on the left menu and then click to the location of the new center of rotation.

Then click on Go though all and the program will go through all the images in the folder. It will create the edited subfolder, where all rotated images will be saved.
After we rotate all measured angles we want to characterize different regions of the image to have the Average grey contrast from the selected region of interest dependent on the external magnetic field. For such an analysis we are going to use another programs - ExtractLoopsFromDrawI32WithSaveTST SAve2.vi. 

Here again, after running the program, it will ask you for the path to the folder of images you want to analyze. Be aware that for the proper running of the software,  you need to have the text file with magnetic fields in the same folder as the images.

To select the region of interest, use the left menu near the image.

Right-click to the image and then select Zoom to fit to see whole image. Then use the magnifier to zoom the desired region.

In the left menu, select the square and draw the region of interest. When holding Ctrl you can select more than one region.

Click on Play to fo through all images at one rotation and get the hysteresis loops from the selected areas.

By click on Export All loops, you will export the text files containing the information about the average grey contrast from the selected area depending on the external magnetic field.
