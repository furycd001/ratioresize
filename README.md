# ratioresize

A simple bash script to resize images while maintaining their aspect ratio.
## Installation

You can use the script in one of two ways:

1. **Copy the Script to `~/.local/bin/`**: For easier access from anywhere in your terminal, copy the script to `~/.local/bin/` and make it executable:
   ```bash
   mv ratioresize ~/.local/bin/ratioresize
   chmod +x ~/.local/bin/ratioresize
   ```
   After this, you can run the script from any directory using:
   ```bash
   ratioresize -h 800
   ```

2. **Run the Script Directly**: If you prefer, you can place the script in a dedicated folder and run it from there:
   ```bash
   chmod +x ratioresize
   ./ratioresize -w 1080
   ```

## Features

- **Aspect Ratio Preservation**: Automatically resizes images while maintaining their original aspect ratio.
- **Support for Multiple Image Formats**: Works with `.jpg`, `.jpeg`, `.png`, `.webp`, and `.avif` image formats.
- **Customizable Output Directory**: The resized images are saved in the `./ratio` directory by default, which is created automatically if it doesn't exist.
- **Invalid Options:** If an invalid option is provided, or if a required argument is missing, the script will display an error message and exit.
- **Processing:** Out of the box the script will only process image files with the extensions `.jpg`, `.jpeg`, `.png`, `.webp`, and `.avif`. You can easily add more yourself.

## Prerequisites

- **ImageMagick**: This script uses the `magick` command from the ImageMagick suite. Make sure ImageMagick is installed on your system.

> To install ImageMagick, please refer to the official [ImageMagick installation guide](https://imagemagick.org/script/download.php).

## Usage

1. **Place Your Images**: Ensure the images you want to resize are located in the current directory where you will run the script.

2. **Run the Script**: Execute the script with the desired dimension option:
    - Resize by height:
      ```bash
      ratioresize -h 800
      ```
    - Resize by width:
      ```bash
      ratioresize -w 800
      ```
> Replace `800` with your desired dimension in pixels.

3. **Check the Output**: The resized images will be saved in the `./ratio` directory. 

## Command Line Options

- `-h <height>`: Resize images to the specified height while maintaining the aspect ratio.
- `-w <width>`: Resize images to the specified width while maintaining the aspect ratio.

## Example

To resize all images in the current directory to a height of 800 pixels:

```bash
ratioresize -h 800
```

> The resized images will be saved in the `./ratio` directory with their original filenames.
