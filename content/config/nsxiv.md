---
title: "Nsxiv"
date: 2023-08-12T19:03:29+01:00
---

---


{{< centered-big-title size="30px" color="#5C5CFF" title="Using the nsxiv Image Viewer" align="center" >}}

{{< centered-big-title size="25px" color="#5C5CFF" title="What is nsxiv?" align="left" >}}


`nsxiv` is a powerful and versatile image viewer designed for efficiency and customization. It provides a feature-rich experience for viewing images and offers customization options to tailor the viewer to your preferences.

{{< centered-big-title size="25px" color="#5C5CFF" title="Why Use nsxiv?" align="left" >}}

- **Feature-Rich:** Explore images with advanced features, such as customizable keybindings and dynamic image operations.
- **Efficient:** `nsxiv` is designed for quick image browsing with a focus on performance.
- **Customizability:** Tailor the viewer to your needs by configuring keybindings, appearance, and more.

{{< centered-big-title size="25px" color="#5C5CFF" title="Installation" align="left" >}}

To install `nsxiv`, you can use the following command:

{{< stylish-code >}}
git clone https://codeberg.org/nsxiv/nsxiv.git
cd nsxiv
sudo make clean install
{{< /stylish-code >}}

Before using `nsxiv`, make sure you have the required dependencies installed 
- Required:

  - Imlib2
  - X11

- Optional :

  - inotify (Auto-reload images on change)
  - libXft , freetype2, fontconfig (Status bar)
  - libexif (Auto-orientation, exif thumbnails)


{{< centered-big-title size="25px" color="#5C5CFF" title="How to Use nsxiv" align="left" >}}

### Basic Usage of `nsxiv`
- Open `nsxiv` in a terminal and pass the directory containing images as an argument.

To view images in a specific directory:

{{< stylish-code >}}
nsxiv [Directory]
nsxiv *
nsxiv image1 image2 ...
{{< /stylish-code >}}




In both image and thumbnail modes, you can use the following commands:

- **q**: Quit nsxiv.
- **Enter**: Switch to thumbnail mode / open selected image in image mode.
- **f**: Toggle fullscreen mode.
- **+**: Zoom in.
- **-**: Zoom out.
- **m**: Mark/unmark the current image.
- **h, j, k, l** (and arrow keys): Navigate selection in thumbnail mode.
- **n, p** (and Space, Backspace): Navigate image list in image mode.
- **h, j, k, l** (and arrow keys): Panning in image mode.
- **a**: Toggle anti-aliasing.
- **ctrl+space**: play gif.


For a more comprehensive list of the default keybinds , refer to the `man` page for `nsxiv`. 


###  
{{< image src="/nsxiv.webp" alt="Alt Text" width="900" height="100" >}}


{{< centered-big-title size="25px" color="#5C5CFF" title="Customizing nsxiv" align="left" >}}

`nsxiv` can be extensively customized through configuration files located in `~/.config/nsxiv/exec`. Here's an overview of each file:

- **image-info**: Displays custom image information in the status bar or overlay.
- **key-handler**: Defines custom keybindings for `nsxiv`, allowing specific actions.
- **thumb-info**: Similar to `image-info`, displays custom information in thumbnail mode.
- **win-title**: Sets the window title, reflecting the viewed image or other relevant data.

you can also edit the `config.h` inside the `nsxiv` folder :

- **config.h**: Customize keybindings, appearance, behavior, and integration . 

{{< centered-big-title size="25px" color="#5C5CFF" title="My Customization" align="left" >}}

# `key-handler`

1. **Delete Image (Ctrl+x d)**: Removes selected images, confirming via `dmenu` with herbe notification.
2. **Copy Image Path (Ctrl+x p)**: Copies the path of the selected image to the clipboard.
3. **Copy Image (Ctrl+x c)**: Copies the selected image as PNG to the clipboard.
4. **Move or copy Image (Ctrl+x m)**: Moves selected images to a chosen directory via `dmenu`.
5. **Image Info (Ctrl+x i)**: Displays detailed image information (filename, size, dimensions, format).
6. **Rename Image (Ctrl+x r)**: Renames selected image via `dmenu` input.
7. **Open Image Directory with nsxiv (Ctrl+x l)**: Prompts a list of image directories and opens the selected directory in `nsxiv`.

# `win-title`

1. **Image Mode**: Reflects filename, image dimensions (width x height), zoom level, and current frame (if applicable).
2. **Thumbnail Mode**: Displays filename and current thumbnail item number out of total items.


# `image-info`

1. **File Size**: Human-readable size of the image file.
2. **Geometry**: Image dimensions (width x height).
3. **Resolution**: Image resolution (dots per inch).
4. **Format**: Image file format (e.g., JPEG, PNG).
5. **File Name**: Name of the loaded image file.


# `thumb-info`

1. **File Size**: Human-readable size of the image file.
2. **File Name**: Name of the image file (extracted using `basename`).   

# `config.h`

1. **Dark Color Scheme**: I've adjusted the colors for a darker theme.
2. **Status Bar**: I resized it for improved visibility and focus.`

# `patches`

1. **color-invert** color inversion using the `i` key.


*Config repository* ...



[*Here you can find a PDF file explaining further my configuration*](/latex/nsxiv.pdf)

	- Formatted using LaTex


---

