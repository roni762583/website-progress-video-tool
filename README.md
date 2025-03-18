# website-progress-video-tool

A tool designed to capture the progress of website development by generating automated screenshots and timelapse videos. It records key updates in real-time, creating visual documentation of the changes made over time. Ideal for tracking design or content adjustments on websites, this tool also integrates with Git for version control, allowing seamless uploading of screenshots and videos to the repository for easy sharing and version tracking.

## Features

- **Automatic Screenshot Capture**: Takes screenshots at specified intervals to track visual progress.
- **Timelapse Video Generation**: Converts the captured screenshots into a timelapse video to showcase the development over time.
- **Integration with Git**: Automatically commits and uploads the screenshots and videos to your Git repository.
- **Customizable Intervals**: Set the frequency at which screenshots are captured.
- **Simple Setup**: Designed for easy integration into your website development workflow.

## Installation

### Prerequisites

- Python 3.x
- Git
- ffmpeg (for video processing)

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/website-progress-video-tool.git
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Ensure `ffmpeg` is installed on your machine. You can download it from [here](https://ffmpeg.org/download.html) or install it via a package manager:
   
   - **Windows**: Follow the instructions on the [FFmpeg website](https://ffmpeg.org/download.html).
   - **macOS**: Use Homebrew:
     ```bash
     brew install ffmpeg
     ```
   - **Linux**: Use APT (for Ubuntu/Debian):
     ```bash
     sudo apt-get install ffmpeg
     ```

4. Run the script to start capturing screenshots and generating videos:

    ```bash
    python capture_progress.py
    ```

## Usage

### Screenshot Interval
By default, the tool captures screenshots every 5 minutes. You can customize the interval by modifying the `interval` variable in the `capture_progress.py` script.

### Output
The screenshots will be saved in the `screenshots/` directory, and a timelapse video will be generated in the same folder as `timelapse.mp4`.

### Git Integration
--scratch-- After each screenshot capture, the tool will automatically commit and push the new files to your Git repository. Make sure to configure your Git username and email for proper commits. --

```python
import git

repo = git.Repo("/path/to/your/repository")
repo.config_writer().set_value("user", "name", "Aharon Zbaida")
repo.config_writer().set_value("user", "email", "roni762583@gmail.com")

Contributing

To contribute to this project, please follow these steps:

    Fork the repository.
    Create a new branch: git checkout -b feature-branch.
    Commit your changes: git commit -am 'Add new feature'.
    Push to the branch: git push origin feature-branch.
    Create a new Pull Request.

License

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.
Author

Aharon Zbaida

Credits

    ChatGPT (OpenAI) for assistance in generating code, content, and documentation.
