# File Organizer

This is a simple command-line utility written in Go that helps you organize files in a specified directory. It automatically sorts files into categorized subfolders based on their file extensions.

## Features

- **Automatic Categorization**: Organizes files into `Images`, `Videos`, `Docs`, `Music`, and `Others` folders.
- **Easy to Use**: Simply provide the target directory path, and the tool handles the rest.
- **Error Handling**: Basic error handling for non-existent directories.

## Supported File Types

- **Images**: `.png`, `.jpg`, `.jpeg`
- **Videos**: `.mp4`, `.mov`, `.avi`, `.amv`
- **Documents**: `.pdf`, `.docx`, `.csv`, `.xlsx`
- **Music**: `.mp3`, `.wav`, `.aac`
- **Others**: Any other file types will be moved to the `Others` folder.

## How to Use

### Prerequisites

- Go (version 1.16 or higher recommended)

### Building the Executable

1. Clone this repository:
   ```bash
   git clone https://github.com/MRQ67/file-organizer.git
   cd file-organizer
   ```

2. Build the executable:
   ```bash
   go build -o file-organizer
   ```

### Running the Application

1. Run the executable from your terminal:
   ```bash
   ./file-organizer
   ```

2. The application will prompt you to enter the path of the folder you want to organize:
   ```
   Give me the folder you want to organizer - 
   ```

3. Enter the absolute path to the directory (e.g., `C:\Users\YourUser\Downloads` or `/home/youruser/Downloads`) and press Enter.

   The tool will then create the necessary subfolders (if they don't exist) and move the files accordingly.

## Example

If you have a folder named `MyUnorganizedFiles` with the following structure:

```
MyUnorganizedFiles/
├── my_photo.jpg
├── vacation_video.mp4
├── report.pdf
├── song.mp3
├── archive.zip
└── another_image.jpeg
```

After running the `file-organizer` and providing `MyUnorganizedFiles` as the target, the structure will become:

```
MyUnorganizedFiles/
├── Images/
│   ├── my_photo.jpg
│   └── another_image.jpeg
├── Videos/
│   └── vacation_video.mp4
├── Docs/
│   └── report.pdf
├── Music/
│   └── song.mp3
└── Others/
    └── archive.zip
```

## Contributing

Feel free to fork the repository, make improvements, and submit pull requests. Any contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.