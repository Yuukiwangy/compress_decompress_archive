# Compress & Extract Archives in Google Colab 📦

![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-brightgreen?style=flat&logo=github)

![Version](https://img.shields.io/badge/version-1.0.0-blue)

![License](https://img.shields.io/badge/license-MIT-yellow)

[![Download Releases](https://img.shields.io/badge/download-releases-orange)](https://github.com/Yuukiwangy/compress_decompress_archive/releases)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Supported Formats](#supported-formats)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Progress Tracking](#progress-tracking)
- [Output Summary](#output-summary)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This repository provides tools to compress and extract ZIP, RAR, 7Z, and TAR files directly in Google Colab. With full progress tracking and output summaries, it is ideal for handling large files and automating archive management in Colab notebooks.

## Features

- Supports multiple archive formats: ZIP, RAR, 7Z, TAR
- Full progress tracking during compression and extraction
- Output summary for quick insights
- Easy integration into Google Colab notebooks
- Handles large files efficiently
- Simple and clear commands

## Supported Formats

This tool supports the following formats:

- **ZIP**: Compress and extract ZIP files with ease.
- **RAR**: Manage RAR files using built-in commands.
- **7Z**: Utilize 7-Zip for high compression ratios.
- **TAR**: Work with TAR files, including gzip and xz compression.

## Installation

To use this tool in your Google Colab notebook, you need to install the necessary packages. Run the following command in a cell:

```python
!pip install py7zr unrar
```

You may also need to install additional libraries based on the formats you wish to work with. For example, to handle RAR files, ensure you have `unrar` installed.

## Usage

Once installed, you can use the following commands to compress or extract files:

### Compressing Files

To compress files into a ZIP archive:

```python
!zip -r my_archive.zip folder_to_compress/
```

To create a RAR archive:

```python
!rar a my_archive.rar folder_to_compress/
```

To create a 7Z archive:

```python
!7z a my_archive.7z folder_to_compress/
```

To create a TAR archive:

```python
!tar -cvf my_archive.tar folder_to_compress/
```

### Extracting Files

To extract files from a ZIP archive:

```python
!unzip my_archive.zip
```

To extract a RAR archive:

```python
!unrar x my_archive.rar
```

To extract a 7Z archive:

```python
!7z x my_archive.7z
```

To extract a TAR archive:

```python
!tar -xvf my_archive.tar
```

## Examples

### Example 1: Compressing a Folder into a ZIP File

```python
import os

# Create a sample folder
os.makedirs('sample_folder', exist_ok=True)
with open('sample_folder/sample_file.txt', 'w') as f:
    f.write('This is a sample file.')

# Compress the folder
!zip -r sample_archive.zip sample_folder/
```

### Example 2: Extracting a ZIP File

```python
# Extract the ZIP file
!unzip sample_archive.zip
```

### Example 3: Compressing a Folder into a 7Z File

```python
# Compress the folder into a 7Z file
!7z a sample_archive.7z sample_folder/
```

### Example 4: Extracting a 7Z File

```python
# Extract the 7Z file
!7z x sample_archive.7z
```

## Progress Tracking

The tool provides real-time progress tracking during compression and extraction. You can monitor the progress in your Colab notebook output. This feature helps you understand how much of the process is complete, especially for large files.

## Output Summary

After each operation, you will receive a summary of the output. This summary includes:

- Total files processed
- Total size of files
- Time taken for the operation

This summary gives you quick insights into the effectiveness of your compression or extraction process.

## Contributing

We welcome contributions to improve this repository. If you have suggestions or want to report issues, please open an issue or submit a pull request. Ensure your code follows the existing style and includes relevant tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, feel free to reach out via GitHub issues or contact the repository owner directly.

[![Download Releases](https://img.shields.io/badge/download-releases-orange)](https://github.com/Yuukiwangy/compress_decompress_archive/releases)

For more updates, check the "Releases" section in the repository.