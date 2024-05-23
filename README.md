# VidDataEncoder

VidDataEncoder is a tool that allows encoding binary data into a video and decoding it back into a binary file. It uses the OpenCV library to handle images and ffmpeg for video creation.

## Requirements

- Node.js (version 12 or higher)
- OpenCV (installed on the system)
- ffmpeg (installed on the system)

## Installation

1. Clone the repository or download the project files.
2. Install the necessary dependencies:

```bash
npm install
```

## Usage

To encode and decode a file, use the following command:

```bash
node index.mjs --input <path_to_input_file> --output <output_file_name>
```

### Example

```bash
node index.mjs --input example.txt --output output_video
```
This command will read example.txt, encode it into a video named output_video.mp4, and then decode the video into a file named output_video_decoded.bin.

## Technical Details
### Encoding

- `encodeDataToVideo(inputFilePath, outputFileName)`: Reads a file, converts its content to binary, and creates a video from the frames generated with the binary data.

### Decoding

- `decodeVideoToData(videoFilePath, outputFilePath)`: Reads a video, extracts the binary data from the frames, and saves it to a binary file.

### Utilities

- `createFrame(binaryData, width, height, frameIndex)`: Creates a black and white frame from the binary data.
- `createFramesDir(framesDir)`: Creates the directory to store frames if it does not exist.

## Notes

- Ensure ffmpeg and OpenCV are correctly installed on your system.
- This project is a proof of concept and may require additional optimizations for production use.

## License

This project is licensed under the GNUv3 License.
