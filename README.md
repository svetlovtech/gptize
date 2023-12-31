# GPTize

**gptize** is a tool for merging the contents of project files into a single text document. It is specifically designed to create datasets that can be loaded into ChatGPT for analysis or training. I, [Aleksey Svetlov](https://www.linkedin.com/in/svetlovtech/), created this tool because I was tired of copying file contents and paths to make GPT understand the context of my project. With gptize, this process is now automated and streamlined.

## Features
- Exception handling for files based on `.gitignore`.
- Support for various encodings when reading files.
- Customizable output file naming based on the input file or directory name.
- Report generation including all processed files.
- Enhanced limit checks for file size and token count, with warnings logged instead of errors raised when limits are exceeded.

## Installation
To install `gptize`, simply use pip:

```bash
pip install gptize
```

This command will install `gptize` and all its dependencies. After installation, you can use `gptize` from the command line anywhere.

## Usage
To run gptize, you have several options:

### Basic Usage
Simply invoke gptize in the command line to process the current directory:
```bash
gptize
```
This will process all files in the current directory and generate a report with a default name like gptize-output-folder-YYYYMMDD-HHMMSS.txt.

### Specifying a Directory
To process a specific directory, use:
```bash
gptize /path/to/directory
```
This will process all files in the specified directory and create a report named gptize-output-folder-YYYYMMDD-HHMMSS.txt.

### Specifying a Single File
For processing a single file:
```bash
gptize /path/to/file.txt
```
This will process only the specified file and generate a report named gptize-output-file_name-YYYYMMDD-HHMMSS.txt, where file_name is the name of the input file.

## Custom Output File
If you want to specify a custom output file name, use the -o or --output option:
```bash
gptize -o custom_output.txt
```
This command will override the default naming convention and use custom_output.txt as the output file name.

## Uploading to ChatGPT
After generating the merged file using `gptize`, you can upload it to ChatGPT for improved context understanding. When making requests to ChatGPT, explicitly reference the uploaded file, for instance, using a phrase like `... based on the imported txt file.` `See project file for context` This approach significantly enhances the quality of ChatGPT's responses by providing it with specific context.

## Components
- `gptizer.py`: The main class for file processing.
- `main.py`: The entry point of the application.
- `models.py`: Data models for files and projects.
- `output_builder.py`: Output constructor for report generation.
- `settings.py`: Project settings.

## Author and Maintainer
[Alexey Svetlov](https://www.linkedin.com/in/svetlovtech/) - Creator and main maintainer.

### Contact Information
- [LinkedIn](https://www.linkedin.com/in/svetlovtech/)
- [Telegram](https://t.me/SvetlovTech)
- Email: alexeysvetlov92@gmail.com

## License
The project is distributed under the [MIT License](LICENSE).
