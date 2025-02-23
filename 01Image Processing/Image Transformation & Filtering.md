<img src='./Images/Image Transformation & Filtering.png'>

# Image Transformation & Filtering

Imagine you have a blurry  or dark image and want to improve its quality. Or maybe you want to highlight specific details, such as the edges of objects. This is where image transformation and filtering come in!

👉 These techniques help us enhance images by adjusting brightness, contrast, removing noise, or even detecting edges.

# 1️⃣ Intensity Transform Functions

An intensity transformation function is a way to modify the pixel values (brightness) of an image.

💡 Think of it like applying filters on Instagram or Photoshop to adjust brightness or contrast!

These transformations can be:
    1️⃣ Linear Transformations - Change brightness and contrast.
    2️⃣ Logarithmic Transformations - Enhance darker details.
    3️⃣ Power-Law Transformations (Gamma Correction) - Adjust brightness non-linearly.

## 📌 (A) Linear Transformations

A simple way to modify an image is using a linear function:
        s = a ⋅ r + b
    
    Where:

    r = Original pixel intensity
    s = New pixel intensity after transformation
    a = Contrast adjustment factor
    b = Brightness adjustment factor

📌 Example:

    Increasing brightness: a=1, b=50 (makes the image brighter)
    Increasing contrast: a=2, b=0 (makes dark areas darker and bright areas brighter)

## 📌 (B) Logarithmic Transformations

This helps brighten dark areas while keeping bright areas unchanged.

        s = c ⋅ log( 1 + r )
    

📌 Example:

    Used in medical images (X- rays) to highlight low-intensity details.

## 📌 (C) Power-Law Transformations (Gamma Correction)

It adjust brightness non-linearly

        s = c ⋅ r^γ 
    
    If γ < 1, it brightens the image.
    If γ > 1, it darkens the image.

📌 Example:

    ✔️ Used in TV displays to adjust brightness properly.

# 2️⃣ Histogram Processing

A histogram is a graph that shows the number of pixels for each intensity level in an image.

💡 Think of it like a bar chart showing how many dark and bright pixels an image has!

