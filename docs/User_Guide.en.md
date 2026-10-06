# MoonStack User Guide

0.3.1 Public Beta | Apple Silicon · macOS 15+ | 2026-10-06

## Install and choose a language

Open `MoonStack-0.3.1-public-beta-macOS15-arm64.dmg` and drag the app into Applications. Launch it from Applications; you can then eject the disk image. Keep the app bundle intact.

On the welcome screen or at the top right of either window, choose English or Simplified Chinese. The default is Simplified Chinese. Your choice is saved and shared between windows. Switching language preserves the current task, paths and adjustment values; it does not recalculate the images.

Raw diagnostic logs retain their original language. Some native file-dialog text follows the macOS language setting. Filenames and paths are never translated.

## System and input requirements

| Item | Requirement or support |
|---|---|
| Mac | Apple Silicon (M series), macOS 15 or later |
| Photos | At least 10 readable RAW files from the same capture sequence |
| Input | Sony ARW, Nikon NEF, Panasonic RW2, Canon CR2 / CR3 / CRW |
| Output | 16-bit TIFF, maximum-quality JPG, or both |

Testing has focused on Sony ARW and macOS 15.8.1. Other camera models and compression modes need further validation. Intel Macs, Windows and video input are not supported by this installer.

## First launch

This beta has not been signed with an Apple Developer ID or notarized. If macOS cannot verify the developer, confirm the download source and compare the file's SHA256 with the release checksum. Follow [Apple's safe-opening guidance](https://support.apple.com/en-us/102445) to check whether Open Anyway is available in System Settings > Privacy & Security.

Stop and report the issue if macOS identifies malware or reports damage. Do not disable system-wide security protections. Grant folder access only for locations you intend to use.

Photos are processed locally and original RAW files are not overwritten. Keep the originals and important exports backed up independently.

<!-- page -->

# 01 Create a stacking task

## Prepare and scan the folder

Use photos from one camera and capture sequence, with similar focal length and exposure. Keep the whole Moon in frame. Separate different nights or substantially different compositions before scanning.

Choose the RAW folder, optionally filter by RAW format, and scan. Review the count, camera information when available, dimensions and reading issues. Only the selected folder's top level is scanned; subfolders, JPGs and sidecar files are not used as RAW input.

Next may remain unavailable if there are fewer than 10 readable frames, unreadable files or inconsistent groups. Separate problematic files and rescan. Renaming an extension does not make an unsupported file readable. A successful scan does not guarantee that every frame will pass full processing.

Do not add, remove or modify input files after scanning. Rescan if the folder changes. Start with 10-20 photos to learn the workflow and allow enough free space for task data as well as exported images.

## Capture interval and output

Enter the time between the start of one exposure and the start of the next, in seconds. Leave it blank if unknown. If the camera waits 1 second after a 1/250-second exposure, enter 1.004. If its interval already means start-to-start time, enter 1. Follow your camera's definition.

Choose an existing writable output parent folder. A new task folder is created for each run. Its actual location appears in Task information when complete.

## Review, start and stop

Keep the default stacking mode and 25% frame-selection target for your first run. A higher percentage does not guarantee more detail. The actual number used also depends on frame quality and processing checks.

Exposure, extra contrast, AI denoising and sharpening start at zero. Adjust these after stacking in the comparison editor.

Review the task, then start stacking. The log shows progress. Preview preparation may continue briefly after the stack completes.

Stopping a task leaves partial files and cannot resume from the interrupted point. Closing the main window or using Cmd+Q also ends processing. A new run creates a new task folder.

<!-- page -->

# 02 Compare and adjust

## Inspect matching lunar detail

The left image is the automatically chosen best single frame. The right image is the stack with live adjustments. Zoom and pan are linked. Choose Fit to window, 100%, 200% or 400%, or use Center Moon.

The left image remains fixed while you adjust the right. Compare the same craters, maria and lunar limb at 100%. Sharpening numbers are not standardized across different applications.

| Control | Use |
|---|---|
| Exposure | -3 to +3 EV. Try -0.3 EV first if bright areas look harsh. |
| Lunar contrast | 0-100%, with Low, Mild, Medium, High and Strong presets. |
| AI denoising | 0-100%; zero is off. Reduce it if fine texture becomes flat. |
| Natural sharpening | 0-100%; zero is off. Reduce it if halos or coarse grain appear. |
| Six wavelet layers | Optional fine adjustment of different detail sizes; begin with the default layer settings. |

## A practical adjustment order

1. Start at zero to inspect the stack without extra adjustments.
2. Set exposure, then increase contrast gradually. Check that bright areas retain tonal separation.
3. Increase sharpening gradually. If noise becomes distracting, add modest denoising and inspect fine texture again.
4. Release the control and wait for the right image to finish updating before exporting.

Reset exposure and Reset contrast affect their respective controls. Reset adjustments returns the main enhancement strengths to zero; use the wavelet reset separately if you changed the layer settings.

Lowering exposure cannot recover texture already clipped during capture. Stacking and enhancement cannot guarantee recovery of detail lost to defocus, movement or atmospheric disturbance. Strong sharpening can amplify noise and halos, while strong denoising can flatten fine texture.

<!-- page -->

# 03 Export and reopen

## Choose TIFF, JPG or both

| Format | Suggested use |
|---|---|
| 16-bit TIFF | Lossless saving of the current result, suitable for archiving and further editing; larger files. |
| Maximum-quality JPG | Convenient for viewing and sharing; still an 8-bit lossy format. |

If unsure, export both. Both files contain the current right-image appearance. After the success message appears, the files are already saved locally. Download links save an additional copy.

A 14-bit RAW and a 16-bit TIFF describe precision at different processing stages. Bit depth alone does not determine image quality. TIFF preserves editing latitude and reduces quantization loss when saving; it does not create detail absent from the originals.

## Find and reopen a result

Task information lists input files, reference frame, task location and export paths. Keep the complete task folder to reopen the editing workflow. TIFF and JPG alone are sufficient for viewing finished images, but cannot restore the full task.

From the main window, open an existing stack result and select the task folder or its result subfolder. Moving or renaming completed task folders may prevent reopening in this beta. Keep them in their original location. Reopening starts the main image-adjustment values at zero; it does not restore the previous editing session. The language preference is saved separately.

## Troubleshooting and feedback

| Symptom | What to check |
|---|---|
| Next is unavailable | Frame count, reading errors and mixed capture groups; then rescan. |
| Highlights look too bright | Lower exposure or contrast; check for clipping in the originals. |
| Halos or rough texture | Reduce sharpening and inspect at 100% zoom. |
| Export fails | Check output permissions and free space; keep a short error message. |

Uninstalling the app does not automatically delete photos or task results. For feedback, use the release repository's Issues page. Include app, system and camera details, the format and frame count, and steps to reproduce. Remove private usernames and full paths from screenshots and logs before posting. Original photos and complete task folders need not be public.

This is a proprietary public beta; application source code is not published. Third-party copyright and license notices are included with the installer. Future free availability or continued maintenance is not guaranteed.
