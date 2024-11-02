
---

# Coursera Course Downloader

This guide will help you set up and use the customized `coursera-dl` tool to download courses from Coursera.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Python**: You can download Python from [python.org](https://www.python.org/downloads/). Ensure you add Python to your system's PATH during installation.
- **pip**: This is included with Python installations starting from version 3.4. If you don't have it, you can find instructions to install it [here](https://pip.pypa.io/en/stable/installation/).

## Getting Your `cauth` String

1. **Log into Coursera**: Open your web browser and go to [Coursera](https://www.coursera.org/). Log in to your account.

2. **Open Developer Tools**:
   - In **Google Chrome**: Right-click anywhere on the page and select **Inspect**, or press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac).
   - In **Firefox**: Right-click on the page and select **Inspect Element**, or press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac).

3. **Navigate to the Application Tab**:
   - In the Developer Tools panel, click on the **Application** tab (in Chrome) or the **Storage** tab (in Firefox).

4. **Find Cookies**:
   - Under the **Cookies** section, find and select `www.coursera.org`.

5. **Locate the `cauth` Cookie**:
   - Look for a cookie named `cauth`. This is your authentication string.
   - **Copy the Value** of the `cauth` cookie.

## Installation

1. Open your command prompt (cmd) or terminal.
2. Run the following command to install `coursera-dl`:

   ```bash
   pip install git+https://github.com/visioncrunch/coursera-dl
   ```

## Downloading Courses

1. Navigate to the folder where you want the course files to be downloaded. You can do this by using the `cd` command. For example:

   ```bash
   cd path\to\your\desired\folder
   ```

2. Run the following command to download the course, replacing `<your_cauth_string>` and `<course_name>` with your actual Coursera `cauth` string and the course name as it appears in the homepage URL of that course:

   ```bash
   coursera-dl --jobs 10 -ca "<your_cauth_string>" <course_name>
   ```

   **Example:**
   ```bash
   coursera-dl --jobs 10 -ca "1FGkyRadOL2bOT4gaMD7IPBi0S5AIeneEcxMrbEzKhmwG7nnu9VzqPliCvZ3J9aJEg2k8Xej8oqf2MYgLCmSRA.owD5wzu4O3AE65AsQ1H7TA.gbi8b2RiH5hTURcWO_K8EOeInWCKnu0Gm_3bLFiAQlaf1vH6l7OfQswwlZvZIR0wXGwy4b43hQpKL1XbZLgkErXIwT0jBqyv50iRpi2LkHp1oKF5kH62qS9l6IpCdHpGPDomsmaSK17iceG5qbbbqX3eHrwJlqbmHMBnetqUG59NrYoXrEsij36rIssrrKRaHlyY5DVDlSL4kiBs5uOaPa89NvZVoHTDzMVkx--poE_KI7QJXL_dKmQAKJLOG5UxfZLFXWt1G4_3ADtIl2Y7HUL124xISS7sdD177twJ9-btlqppza8j2YRtgqLSOt9o9xFdFAGT5TtRGlIR_18D84DLR7Y2bLQ9Nt2NArPx9xGdJF5nz55mFeOfTU7vKLx5xnOgUCILCnUBe-9NM4238q_ciFKF2_C9VyoyLpsG4pWJ6b0xxBsOweE5Sx2VjSQP" relational-database-management-systems
   ```

3. Wait for the course to download. The tool will handle downloading all course materials, and you will see the progress in your command prompt.

## Troubleshooting

- If you encounter issues with the download, ensure that your `cauth` string is correct and that the course name matches the course URL on Coursera.
- Check your internet connection if the download fails unexpectedly.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
