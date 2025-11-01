[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IndrajithGamage/onahupcnv/blob/main/OnaHuptak_Convert.ipynb)

# Indrajith Video Converter for Google Colab

This repository contains a Google Colab notebook for high-quality, high-speed video conversion using `ffmpeg`. It provides a simple user interface to control complex `ffmpeg` settings for encoding, scaling, and watermarking.

---

## 🚀 How to Use

1.  **Enable GPU:** After opening in Colab, go to **Runtime** > **Change runtime type** and select **T4 GPU** (or any available GPU) from the "Hardware accelerator" dropdown. This is required for the fast `nvenc` encoders. Using the official short link https://bit.ly/onahupcnv opens the GPU runtime directly. 
2.  **Mount Google Drive:** The notebook needs to access your files. When running the cell, provide access to mount your Google drive. This is completely safe and private. 
3.  **Set File Paths:** Update the `input_file` and `output_file` variables to point to your video.
4.  **Choose Settings:** Use the interactive form to select your desired encoder, resolution, and quality (CRF or Bitrate).
5.  **Run:** Run the main cell to start the conversion. Progress will be displayed below the cell.

---

## ✨ Features

* **Multiple Encoders:**
    * `h264_nvenc` (Fast, GPU-accelerated)
    * `hevc_nvenc` (Good compression, GPU-accelerated)
    * `libx264` (High quality, CPU-based)
    * `libx265` (Best compression, CPU-based)
* **Quality Control:** Choose between **CRF** (constant quality) or **Bitrate** (constant file size) modes.
* **Advanced Scaling:** High-quality `lanczos` scaling to any resolution, including portrait and landscape presets.
* **Dynamic Watermarking:** (Optional) Add a sliding text watermark to your video.
* **File Comparison:** Automatically shows the original vs. processed file size and bitrate.

---

## ⚙️ Configuration Options

* **Resolution:** Choose from presets like 1080p/720p or set a custom width and height.
* **Quality (CRF/Bitrate):**
    * **CRF:** Lower values mean higher quality (e.g., 20-25).
    * **Bitrate:** Set a target (e.g., `2500k`) for predictable file sizes.
* **Preset Speed:** `medium` is a good balance. `slower` provides better compression but takes more time.
* **Tune:** Optimize the encode for content like `film` or `animation`.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



