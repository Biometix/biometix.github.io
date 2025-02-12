---
layout: page
title: FAQ
nav_order: 8
permalink: /faq/
---


# Frequently Asked Questions (FAQ)

## How do I specify input folder that has spaces in the name?

For BQAT-CLI, if your input folder name has spaces, you need to add a escape character ("\\" in Linux), and enclose the path with quotation marks:

``` sh
# For example if the path to the folder is [data/input folder/]:
./run.sh -M face -I "data/input\ folder/"
```

## How do I install Docker?

To install Docker, follow these steps:

- Download [Docker Desktop](https://www.docker.com/) for an easy-to-use graphical interface or [Docker Engine](https://docs.docker.com/engine/install/) for command-line installation.
- Follow the instructions provided on the official website. Note: You may need to sign up to get full access to Docker Desktop.

## How do I start the Terminal to run scripts or Docker?

**For Windows users:**
  - Press `Win + R` to open the Run dialog.
  - Type `cmd` or `powershell` and press Enter.

**For Mac users:**
  - Press `Cmd + Space` to open Spotlight Search.
  - Type `Terminal` and press Enter.

**For Linux users:**
  - Depending on the Linux distribution:
    - Press `Ctrl + Alt + T`.
    - Use a shortcut specific to your desktop environment.
    - Search for "Terminal" in the application menu.

## How can I retrieve results when using the Web GUI interface?

Follow these steps to obtain results using the Web GUI interface:

1. Open your browser and visit the URL displayed in the terminal.
2. Drag or upload your images to the designated upload area.
3. Choose the desired model and click the "Submit" button.
4. Check the status of the task by clicking "Get Output." Wait until the task is marked as finished.
5. Press "Get Output" again, and export the data from the bottom of the page.

## I encountered permission issues when running BQAT in the terminal. What should I do?

If you encounter permission issues, try the following:

- Prefix the command with `sudo` to run it with elevated privileges. For example:

  ```sh
  sudo your_bqat_command_here
  ```

## If you see this error `Error: Got unexpected extra argument`, it means there is space in the filepath.

Wrap it with double quotes and escape the space. Refer to the example below:

e.g. input folder is `data/iris folder/`
```sh
./run.sh --input "data/iris\ folder/" --mode iris
```

## BQAT-CLI see error related to ray worker died.

If you encounter error related to worker died, that might indicates the machine don't have sufficient RAM to work with CPU cores. Usually that happens on Windows where the it allocates [50% of available RAM](https://docs.docker.com/desktop/settings-and-maintenance/settings/#:~:text=By%20default%2C%20Docker%20Desktop%20is,decrease%20it%2C%20lower%20the%20number.) to Docker engine. You may limit the CPU or allocate more memory to it.

## OFIQ engine very slow to get result.

Due to the nature of OFIQ engine workflow, each time it was called, there is a initialisation process which will take significant time to load the underlying models (4~7s), whereas the actual processing time of the image take 300~500ms. As a result, if you send the image one by one, the response time will be 4~7s per image, while the speed of bulk processing will be 0.4~0.6s per image.

## BQAT-Stateless failed to respond.

The server is operating on a best-effort basis, which means it does not monitor status of the workers. In some cases where there are too many request sent to the server and there are too many workers trying to handle the request, the container/process may crash due to OOM error.

Although docker engine will restart the container, you might still need a load balancing mechanism implement in the upstream workflow. Or you may config to allow only one request per container and handle parallelism at container level.


{: .highlight }
> Let us know if you have question or new idea in the discussion board, or reach out to [us](https://biometix.github.io/about/#about-us) for [advance support](https://biometix.github.io/index/advance_support.html)!
