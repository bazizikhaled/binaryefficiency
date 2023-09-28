---
title: "Sent"
date: 2023-08-10T07:52:47+01:00
---

---



{{< centered-big-title size="30px" color="#be4d25" title="Using the sent Presentation Tool" align="center" >}}

{{< centered-big-title size="25px" color="#be4d25" title="What is sent?" align="left" >}}


`sent` is a simple, lightweight, and command-line-based presentation tool. It allows you to create slideshows by using plain text files, making it easy to focus on the content of your presentation.

{{< centered-big-title size="25px" color="#be4d25" title="Why Use sent?" align="left" >}}

- **Simplicity:** Creating slides is as easy as writing paragraphs in a text file.
- **Minimal Distraction:** No need to worry about design, animations, or complex slide transitions.
- **Lightweight:** `sent` is lightweight and efficient, making it a great choice for quick presentations.

{{< centered-big-title size="25px" color="#be4d25" title="Installation" align="left" >}}

To install `sent` , you can use the following command:

{{< stylish-code >}}
git clone https://git.suckless.org/sent
cd sent
sudo make clean install
{{< /stylish-code >}}

Before using `sent`, make sure you have the required dependencies installed, which are `libx11`,`libxft` and `farbfeld`

{{< stylish-code height="0.5" size="20px"  >}}
sudo pacman -S libx11 libxft
{{< /stylish-code >}}
`farbfeld` for the images to render
{{< stylish-code  >}}
git clone https://git.suckless.org/farbfeld
cd farbfeld
sudo make clean install
{{< /stylish-code >}}


{{< centered-big-title size="25px" color="#be4d25" title="How to Use sent" align="left" >}}

### To create and run a presentation using `sent`
- in a text file Each slide is separated by a blank line
- Use lines starting with `#` for comments.
- Use `@FILENAME` to add an image slide, e.g., `@slide.png`.
- `\`  for empty slides

To run the presentation, use the following command:


{{< stylish-code height="0.5" size="20px">}}
  sent [File]  
{{< /stylish-code >}}

{{< centered-big-title size="25px" color="#be4d25" title="Example" align="left" >}}


{{< image-left src="/sent.gif" alt="Alt text" width="600px" margin="50px" >}}
{{< stylish-code  height="1" size="20px">}}
# Slide 1: This is a comment
 Introduction to Sent

Sent is a minimalistic and lightweight presentation tool.

Sent:
- Plain text slides: Create slides with plain text content.
- Image slides: Include images to illustrate your points.
- Use lines starting with # for comments

# Image Slide
@image1.jpg

👋 Hello, world! 🌍

Sent allows basic customization using a configuration file.

@image2.jpg
{{< /stylish-code >}}

{{< /image-left>}}


{{< centered-big-title size="25px" color="#be4d25" title="Patching" align="left" >}}

Patching is a method used to modify or extend software without altering the original source code. In the context of 
`sent`, patching allows you to customize its behavior, add new features, or fix issues while still being able to update 
the software.


1. **Download the Patch** : [`suckless sent patches`](https://tools.suckless.org/sent/patches)

2. **Apply the Patch**:

   Open a terminal and navigate to the directory where the `sent` source code is located. Apply the patch using the 
   `patch` command:

{{< stylish-code height="1" size="17px">}}
patch -i [path_to_patch_file]
sudo cp config.def.h config.h
{{< /stylish-code >}}

   This command applies the changes specified in the patch file to the `sent` source code.

4. **Compile `sent`**:

   Recompile the modified `sent` source code to generate the patched executable:

{{< stylish-code height="0.5" size="20px">}}
sudo make install
{{< /stylish-code >}}




{{< centered-big-title size="25px" color="#be4d25" title="what i patch" align="left" >}}


1. **Inverted Colors** (`sent-invertedcolors-72d33d4.diff`):
   - Inverts the color scheme, offering high contrast mode with the `i` key.

2. **PDF Export** (`sent-pdf-2649e8d.diff`):
   - Adds direct PDF export using the `g` key.

3. **Progress Bar** (`sent-progress-bar-1.0.diff`):
   - Includes a progress bar to track slide position.

4. **Toggle Color Scheme** (`sent-toggle-scm-20210119-2be4210.diff`):
   - Toggles between normal and inverted color modes with the `i` key.

{{< centered-big-title size="25px" color="#be4d25" title="Get My Configuration" align="left" >}}

simply clone the repository and compile : 

{{< center alt="text"  src="/under.gif">}}



---
