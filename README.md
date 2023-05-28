# SD and Segment Anything

Generate Images using Stable Diffusion combined with segment anything model to select different parts of images and let us change them using a prompt.

## Installation
The code requires `python>=3.8`, as well as `pytorch>=1.7` and `torchvision>=0.8`. Please follow the instructions [here](https://pytorch.org/get-started/locally/) to install both PyTorch and TorchVision dependencies. Installing both PyTorch and TorchVision with CUDA support is strongly recommended.

Install Segment Anything:

```
pip install git+https://github.com/facebookresearch/segment-anything.git
```
Then install required requirements using:
```
pip install -r requirements.txt
```

Click the links below to download the checkpoint for the corresponding model type.

- **`default` or `vit_h`: [ViT-H SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth)**
- `vit_l`: [ViT-L SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_l_0b3195.pth)
- `vit_b`: [ViT-B SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth)


## Usage

1. Make sure the dependencies are installed.
2. Run the code app.py using a Python interpreter.
3. The GUI will open, displaying the input image, mask image, output image, and prompt textbox.
4. Select pixels on the input image to generate a mask using the "Input" image selection.
5. Enter a prompt in the textbox.
6. Click the "Submit" button to perform the inpainting.
7. The output image will be displayed in the "Output" image component.

Note: The code assumes that the SAM checkpoint file and the StableDiffusionInpaintPipeline pretrained model are available in the specified locations. Adjust the paths accordingly if needed.