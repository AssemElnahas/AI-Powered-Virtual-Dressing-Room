# AI-Powered Virtual Dressing Room

This Streamlit application allows users to upload their photos and clothing items, which are then processed to create a virtual try-on experience. The app removes the background from the user’s image, overlays the clothing item on the user’s image, and displays the final result. The user can then download the final image to see how the clothing fits them.

## Features

- **Upload User Photo**: Upload a photo of yourself (PNG/JPG/JPEG).
- **Upload Clothing Item**: Upload a photo of a clothing item you wish to try on.
- **Background Removal**: The app removes the background from the user’s photo using simple image processing techniques (can be enhanced with deep learning models).
- **Clothing Overlay**: The app overlays the uploaded clothing onto the user’s photo for a virtual try-on.
- **Download Image**: The final virtual try-on image can be downloaded for further use.

## Requirements

To run this project, you need to have Python and the following libraries installed:

- `streamlit`
- `opencv-python`
- `numpy`
- `Pillow`

You can install the required libraries using pip:

```bash
pip install streamlit opencv-python numpy Pillow
```

## How to Run

1. Clone or download the repository to your local machine.
2. Navigate to the folder where the script is located in your terminal.
3. Run the script using the following command:

```bash
streamlit run AI-Powered_Virtual_Dressing_Room.py
```

4. Once the app is running, open the provided URL in your browser.
5. Upload your photo and clothing image via the sidebar.
6. The app will process the images and show the results: background removal and clothing overlay.
7. Optionally, you can download the final image by clicking the download button.

## How It Works

1. **Background Removal**: The background removal function takes the user’s photo and performs basic image processing using OpenCV. The background is removed by converting the image to grayscale and applying a binary threshold to create a mask. The background is then removed using bitwise operations.
   
2. **Clothing Overlay**: The clothing image is resized to match the dimensions of the user’s photo. A basic overlay is applied using `cv2.addWeighted` to combine the user’s photo with the clothing image at a specified transparency level.

3. **Streamlit Interface**: The app uses Streamlit to create an easy-to-use interface where users can upload images and view the results in real-time. The final result is displayed on the web page and can be downloaded.

## Future Improvements

- Implement more advanced background removal using deep learning models like U²Net or Mediapipe for more accurate segmentation.
- Enhance the clothing overlay logic to better fit different clothing types and user body shapes.
- Add the ability to rotate and scale the clothing item for better alignment.

## License

This project is open source and available under the [MIT License](LICENSE).
