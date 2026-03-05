---
name: screen-logger
description: Automatically take a screenshot using macOS built-in tools, read it, analyze the user's current working state, and append a summary with a timestamp to an activity log text file.
---

# Screen Logger Skill

When the user asks you to run the "screen-logger" skill, you must perform the following actions in order:

1. **Take a Screenshot:**
   Use the `run_command` tool to execute the macOS screen capture command silently (`-x`). Save the screenshot to a temporary file in the current working directory, for example `./capture_temp.png`.
   ```bash
   screencapture -x ./capture_temp.png
   ```

2. **Read the Screenshot:**
   Use the `view_file` tool to open `./capture_temp.png` (you may need to resolve this to an absolute path first). Your vision capabilities will process the image so you can analyze the screen's contents.

3. **Analyze Current Activity:**
   Based on the contents of the screenshot, formulate a brief summary (about 1-2 sentences) of what the user is currently doing. Identify the main application in focus, any visible code/design context, and what tasks appear to be underway.

4. **Append to Log File:**
   Use the `run_command` tool to append your analysis along with the current timestamp to `activity_log.txt` in the current directory.
   Example command:
   ```bash
   echo "$(date '+%Y-%m-%d %H:%M:%S') - [Your short activity summary here]" >> ./activity_log.txt
   ```
   *Note: Do not literally output the brackets, replace them with your actual summarized text.*

5. **Cleanup:**
   Use the `run_command` tool to delete the temporary screenshot so it doesn't clutter the project.
   ```bash
   rm ./capture_temp.png
   ```

Once the log is appended and the temporary file is deleted, you have successfully completed this workflow.
