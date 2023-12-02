# Diffusion_Model_With_NeRF

## Contributors

Omar El Khalifi, Dune AMR--TARDIF

## How does it work

Our pipeline consists in :
1) Generate an image of a clear subject on a white background using stable diffusion
2) Change the perspective slightly and crop the image (not implemented in python, we used an external tool)
3) Run the computing_mask and plug in the warped image, chosing the edges that match the perspective shift (right edge for right motion)
4) Feed back the mask and the warped image to stable diffusion with the inpainting option
5) Repeate multiple times and feed the generated images to the nerf model (does not work)

Our own script :
- The computing_mask notebook that needs to be fed the right image (in the third cell)


Since we used a lot of external tools that often way to much to be shared here are included all the parts of our pipeline :
- Stable diffusion : https://github.com/AUTOMATIC1111/stable-diffusion-webui
- Vanilla Nerf + TinyNerf : https://github.com/bmild/nerf
- Plenoxels

## Project

See PDF report
