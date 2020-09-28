# Video GIF Capture Spec

## 1. Overview

### 1.1. Executive Summary

Users are evolving to need to share more than just static images of their desktop. Given this fact, there becomes a need for a light-weight tool beyond the standard screenshot technologies that allows quick and easy screen recordings. Such tooling can enable an increased range of creative license for users to develop the visual experiences that truly bring their visions to life. While there is 3rd party software that exists for this purpose, these tools tend to provide overly complex functionalities that are excessive for simple use cases. Therefore, this document proposes the development of a lightweight, native Windows alternative to allow for fast and straight-forward screen recording and editing. This would allow for increased productivity and offer a familiar and intuitive UI experience based on similar Windows Shell tooling for easy onboarding.

### 1.2. Goals and Non-Goals

Goals:

* Create simple, lightweight recording tool
* Export to known visual standard format based on the desired usage

Non-goals:

* End to end complex editor
* Transcode existing items to GIF
* Transcode GIF to video
* Ability to open/edit prior recordings

### 1.3. Key Definitions/Concepts

Here are definitions of words and acronyms found throughout this document to ensure clarity:

* **VGC:** Video GIF Capture  –  The tentative name for this PowerToy.

### 1.4. Narrative / Scenarios

#### 1.4.1. Example Use Cases

* Creating animated visuals for instructions/tutorials: Quickly capture relevant clips from videos or animations, which can be easily converted to a GIF and pasted into the documentation.
* Improved bug reporting on GitHub: Select the application to be recorded and capture the usage that causes the bug/crash in the program. Convert the recording to a GIF and attach it to the bug report.
* IT & administrative guidance: Easily record desktop to showcase the appropriate steps for proper machine configurations. Save the recording as a video and upload to desired distribution channels.
* Light-weight media alternatives: For sharing large media like 3D models, pictures and videos can be more effective than exporting the entire model itself. Using VGC, users can quickly record interactions with the model and save it as a video for export.
* Meme creation: Capture a snippet of a video, quickly trim and add text to the clip, and convert it to a GIF to share through popular social media.

#### 1.4.2. Key Scenarios

**GitHub Bug Reporting:** When reporting bugs or issues against a GitHub repository, it is often helpful for users to be able to attach visuals of the experience for developers to more easily reproduce and diagnose the issue. In many cases, a short recording of the application’s behavior is much more beneficial than screenshots or textual descriptions of the problem. With GitHub’s capacity to embed GIFs in the bug reports, Video GIF Capture is an ideal tool for quickly and seamlessly recording the application’s behavior, converting that recording to a GIF, and attaching the GIF to the GitHub bug log.
Outcome from Using VGC for Reporting: A successful VGC would enable a user to quickly launch and isolate the recording’s focus on the faulty application through window selection. Once the recording’s positioning is set, users can capture the application’s behavior through a familiar “Play/Pause/Stop” interface. After recording, a simplistic editor is loaded with an intuitive scrubbing bar for fast video trimming. Once editing is complete, the recording can then be copied to the clipboard as a GIF and pasted into the bug report.

**IT & Administrative Guidance:** Utilizing corporate devices and networks often requires tedious configuration steps to make sure proper authorizations can be granted to users. Typically, instructions of this nature are distributed through static documentation. With the assistance of VGC, visually guided steps can be generated to greatly improve the quality of instruction and reduce the likelihood of errors from misinterpretation.
Outcome from Using VGC for IT Guidance: A successful VGC would enable IT & administrators to begin a recording that captures their desktop screen. With the appropriate recording options set, VGC should capture all windows that are interacted with, in addition to overlaying the screen with guided keystrokes as they are pressed by the user. After recording, the user should then be able to trim the video and add optional text overlay as needed for clarification. Once editing is complete, the user should be able to save the final recording to the desired video format and export for distribution.

### 1.5. Existing Landscape

| Category | Xbox Game Bar | ScreenToGIF | Camtasia | SnagIt | Snip and Sketch | Video GIF Capture |
| -----    | -----         | -----       |  -----   | -----  | -----           | -----             |
| Free                                       |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Launch Application via Keyboard Shortcuts  | ![Y](./images/GIFSpec/Y.png "Yes")|![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Click-And-Drag Rectangular Section Capture |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Specific Recorded Window Capture           |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Full Screen Capture                        |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Explicit Recording Dimensions Capture      |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Trim Recording                             |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Add Text Overlay to Recording              |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| System Audio                               |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Optional Cursor Capture                    |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Keystroke Capture                          |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Save to MP4                                |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Save to GIF                                |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |
| Copy Captured Media to Clipboard           |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |
| Microphone Audio                           |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |
| Webcam Capture                             |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |
| Frame by Frame Editing                     |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |
| Edit Out Middle Sections from Recording    |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |
| Add CGI Effects during Editing             |![N](./images/GIFSpec/N.png "No") |![Y](./images/GIFSpec/Y.png "Yes") |![Y](./images/GIFSpec/Y.png "Yes") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No") |![N](./images/GIFSpec/N.png "No")|

The following subsections of **1.5.** describe insights into the user experience of capturing a recording with existing software.

###### *Figure 1.5.1 - Original state of example screen to be recorded.*

![BaseScreen](./images/GIFSpec/BaseScreen.png "Screenshot of Halo Infinite Video")

#### 1.5.1. Xbox Game Bar

[Xbox Game Bar](https://www.microsoft.com/en-us/p/xbox-game-bar/9nzkpstsnw4p?activetab=pivot:overviewtab) is a native Windows application that allows users to record their full screen by simply pressing the key binding: Win + Alt + R, for both starting and stopping the recording. A minimalistic recording widget is displayed while recording (Figure 1.5.2), yet removed from the final recording when played in the app’s gallery (Figure 1.5.3). Note that the gallery is accessed through the Xbox Game Bar menu (launched via Win + G), which includes a host of various options, settings, and metrics. To trim the recording, Xbox Game Bar’s interface has the user click through its gallery window, File Explorer, the Movies and TV app, and the Photos app before trimming functionality can be accessed (Figure 1.5.4).

###### *Figure 1.5.2 – Xbox Game Bar Recording Widget*

![XGBRecording](./images/GIFSpec/xboxGBRecordingWidget.png "Xbox Game Bar Recording Widget")

###### *Figure 1.5.3 – Gallery Window in Xbox Game Bar*

![XGBGallery](./images/GIFSpec/xboxGBGallery.png "Screenshot of Xbox Game Bar Gallery accessed from HUD")

###### *Figure 1.5.4 – Trimming video via Xbox Game Bar. Note that the editing process takes the user through File Explorer, Movies & TV, and Photos before accessing the trimming functionality.*

![XGBTrimming](./images/GIFSpec/xboxGBTrimming.png "Screenshot of video trimming via Xbox Game Bar")

#### 1.5.2. ScreenToGIF

[ScreenToGIF](https://www.screentogif.com/) is a free application that allows users to record a section of their screen. The launch menu (Figure 1.5.5) features a minimalistic set of options, and the recording interface (Figure 1.5.6) allows the user to drag and modify the bounding box around the desired content prior to recording. Note that there was a noticeable delay in the time from stopping the recording to opening the editing window as compared to other applications. Also note the verbose set of functionalities and editing options available in ScreenToGIF’s editing window (Figure 1.5.7).

###### *Figure 1.5.5 - ScreenToGIF Launch Menu*

![STGMenu](./images/GIFSpec/StGMenu.png "Screenshot of ScreenToGIF's launch menu")

###### *Figure 1.5.6 - ScreenToGIF Recording Interface*

![STGRecording](./images/GIFSpec/StGRecording.png "Screenshot of ScreenToGIF's recording interface")

###### *Figure 1.5.7 - ScreenToGIF Editing Window*

![STGEditing](./images/GIFSpec/StGEditing.png "ScreenToGIF's editing window")

#### 1.5.3. Camtasia

[Camtasia](https://filmora.wondershare.net/filmora-video-editor-bing.html?msclkid=98c2e7e5340f15bf2c9cb8853f3ed3af&utm_source=bing&utm_medium=cpc&utm_campaign=Filmora_SS_pid(1107)_US_Bing&utm_term=camtasia&utm_content=3.%20CP-Camtasia) is a paid software that provides users with an extensive set of high-end recording and editing features. The recording interface (Figure 1.5.8) offers a rich set of controls and settings that enable the user to capture a multitude of different media assets. The editing window (Figure 1.5.9) includes a verbose set options ranging from trimming capabilities to CGI and transition effects. Note the video export options (Figure 1.5.10) Camtasia supports offer popular MP4 formats and social media sharing options, in addition to GIF support under ‘Custom production settings’.

###### *Figure 1.5.8 - Camtasia's Recording Interface*

![CamtasiaRecording](./images/GIFSpec/camtasiaRecording.png "Screenshot of Camtasia's recording interface")

###### *Figure 1.5.9 - Camtasia's Editing Window*

![CamtasiaEditing](./images/GIFSpec/camtasiaEditing.png "Camtasia's editing menu")

###### *Figure 1.5.10 - Camtasia's video export options*

![CamtasiaExporting](./images/GIFSpec/camtasiaExporting.png "Camtasia's video export options")

#### 1.5.4. Snip and Sketch

[Snip and Sketch](https://www.microsoft.com/en-us/p/snip-sketch/9mz95kl8mr0l?activetab=pivot:overviewtab) is a native Windows application that allows users to select sections of their screen to capture images of. While Snip and Sketch does not include recording functionality, we note this application because it captures the essence of simplicity and efficiency we hope to replicate in Video GIF Capture. Snip and Sketch’s intuitive interface (Figure 1.5.11) is quickly launched via the OS level key binding: Win + Shift + S. By selecting each option, the user easily becomes familiar with the range of applications. Once a section is captured, the image is immediately copied to the clipboard for usage in other applications. Snip and Sketch’s typical interaction time only takes a matter of seconds.

###### *Figure 1.5.11 - Snip and Sketch Selection Interface*

![Snip & Sketch](./images/GIFSpec/SnipAndSketch.png "Snip & Sketch Screenshot")

### 1.6. Opportunity for Impact

Given the software discussed in [**1.5 - Existing Landscape**](#15-Existing-Landscape), we aim to target Video GIF Capture as a lightweight, Windows native alternative to more verbose, feature-heavy applications like ScreenToGIF and Camtasia. Following Snip and Sketch’s intuitive and simple styling, Video GIF Capture should enable users to quickly ramp-up on its usage, and offer concise, efficient recording/editing options for common use cases as described in [**1.4 – Narrative / Scenarios**](#14-narrative--scenarios). By leveraging Windows native UI, we can create a familiar interaction experience that feels at home with similar Windows applications like Snip and Sketch, Xbox Game Bar, the Movies and TV app, and the Photos App. With an explicit focus on screen recording, we aim to streamline the user interface so that the overall time spent on the application can be comparable to Snip and Sketch’s fast interface, yet functionally equivalent to lightweight workloads on ScreenToGIF and Camtasia.

## 2. Definition of Success

### 2.1. Customers

Video GIF Capture is for power users and developers who are looking to tune and streamline their Windows experience for greater productivity and enhanced user experience.

### 2.2. Expected Impact: Customer, and Technology Outcomes

* **High Reliability:** Less than 0.1% crash rate.
* **High User Retention:** 25% or more of active PowerToys users who used VGC, use it again within 28 days.

## 3. Requirements

### 3.1. Functional Requirements

#### 3.1.1. Functional Requirements Overview

|No. | Requirement | Pri|
| - | - | - |
|1 | VGC launched via OS-Level key shortcut: Win + Shift + R.| P0 |
|2 | VGC launched alternatively through PowerToys settings menu launch button. | P0 |
|3 | On launch, overlay an intuitive action menu for region capture selection. | P0 |
|4 | Once a region is selected, transition the displayed action menu to populate with recording options. | P0 |
|5 | Once a recording is stopped, load the captured media in an editing window. | P0 |
|6 | Once editing is completed, save recording to desired format. | P0 |
|7 | At any point, the user should be able to close VGC, returning machine to original state. | P0 |

#### 3.1.2. Region Capture Selection Capture

|No. | Requirement | Pri
| - | - | - |
|1 | On launch, display region capture selection options: Rectangular Selection, Window Selection, Full Screen Selection, Exact Coordinates Selection & Cancel. Styling should resemble that of the Snip and Sketch tool ([Figure 1.5.11](#figure-1511---snip-and-sketch-selection-interface)) and possess the options layout of the Selection Menu Mock-Up ([Figure 3.2.1](#figure-321---mock-up-of-video-gif-capture-selection-menu)). | P0 |
|2 | Dim the background so the screen capture menu is in focus. | P0 |
|3 | Default mode is Rectangular Selection. | P0 |
|4 | Transition to the other selection modes via clicking the option’s corresponding button in the menu. | P0 |
|5 | Alternatively transition to the other selection modes via the Tab key. | P0 |
|6 | To cancel selection mode and close the VGC app, click the cancel button or press the OS-Level Key Shortcut: Win + Shift + R. | P0 |
|7 | Alternatively cancel selection mode and close the VGC app via pressing the ESC key. | P0 |
|8 | Once a region has been selected. Transition the menu interface to populate with options for recording as illustrated in [Figure 3.2.3](#figure-323---mock-up-of-video-gif-capture-recording-interface-prior-to-recording). | P0 |

#### 3.1.3. Rectangular Selection

|No. | Requirement | Pri
| - | - | - |
|1 | In this mode, click and drag cursor over the desired region, displaying a highlighted border for visual confirmation like that of Camtasia’s bounding box in [Figure 1.5.8](#figure-158---camtasias-recording-interface). | P0 |
|2 | Transition the selection menu to populate with recording options ([Figure 3.2.3](#figure-323---mock-up-of-video-gif-capture-recording-interface-prior-to-recording)). | P0 |

#### 3.1.4. Window/Application Selection

|No. | Requirement | Pri
| - | - | - |
|1 | In this mode, move the cursor across the screen, highlighting whatever window the cursor is currently hovering over. | P0 |
|2 | Clicking on desired window causes it to come in focus, displaying a highlighted border for visual confirmation like that of Camtasia’s bounding box in [Figure 1.5.8](#figure-158---camtasias-recording-interface). | P0 |
|3 | Transition the selection menu to populate with recording options ([Figure 3.2.3](#figure-323---mock-up-of-video-gif-capture-recording-interface-prior-to-recording)). | P0 |

#### 3.1.5. Full Screen Selection

|No. | Requirement | Pri
| - | - | - |
|1 | In this mode, simply click the screen to confirm the recording selection. | P0 |
|2 | In the case of multi-monitor displays. The screen that the cursor is currently located when clicking will be captured, displaying visual confirmation around the perimeter of the screen like that of Camtasia’s bounding box in [Figure 1.5.8](#figure-158---camtasias-recording-interface). | P0 |
|3 | Transition the selection menu to populate with recording options ([Figure 3.2.3](#figure-323---mock-up-of-video-gif-capture-recording-interface-prior-to-recording)). | P0 |

#### 3.1.6. Exact Coordinates Selection

|No. | Requirement | Pri
| - | - | - |
|1 | In this mode, an additional drop-down panel from the selection menu should appear that displays the inputs: X, Y, Height, Width, and Confirm ([Figure 3.2.2](#figure-322---mock-up-of-video-gif-capture-expanded-selection-menu-for-exact-coordinate-selection)). | P0 |
|2 | A highlighted rectangular border will be produced on the screen, of dimensions “Height” x “Width”, with the top-left corner of the border located at coordinate (X, Y) on the screen. Visualization equivalent to Camtasia’s bounding box in [Figure 1.5.8](#figure-158---camtasias-recording-interface). | P0 |
|3 | The inputs can be adjusted textually via their corresponding text fields in the drop-down. | P0 |
|4 | The inputs can also be adjusted manually via click-and-dragging the displayed tooltips along the highlighted border. | P0 |
|5 | Dragging the tooltips located on the border’s corners will preserve the region’s current aspect-ratio while adjusting its size. | P0 |
|6 | Selecting the ‘Confirm’ button from the drop-down menu causes the highlighted border to become locked in as the selection menu transitions to populate with recording options. | P0 |

#### 3.1.7. Recording

|No. | Requirement | Pri
| - | - | - |
|1 | Populate the selection menu with recording options: Record, Cancel ([Figure 3.2.3](#figure-323---mock-up-of-video-gif-capture-recording-interface-prior-to-recording)). | P0 |
|2 | Keep the highlighted border around the selected recording region but remove the dimmed background effect that was created when the selection tool was activated. | P0 |
|3 | Allow the user to interact with the system as needed to prepare for the initiation of the recording. | P0 |
|4 | Allow the user to manually modify the recording region prior to the initiation of recording via click-and-drag functionality on the highlighted border like Camtasia’s bounding box in [Figure 1.5.8](#figure-158---camtasias-recording-interface). | P0 |
|5 | When ‘Play’ is selected, lock the highlighted border so that it can no longer be adjusted. | P0 |
|6 | When ‘Play’ is selected, overlay the screen with a visual count-down, immediately followed by the initiation of the recording. | P0 |
|7 |Alternatively start recording by pressing the OS level short-cut: Win + Shift + R. | P0 |
|8 | When recording begins, transition the recording menu to the active state as depicted in [Figure 3.2.4](#figure-324---mock-up-of-video-gif-capture-recording-interface-during-recording). | P0 |
|9 | While the recording is active, the user is free to interact with the system as desired. | P0 |
|10| When the user selects the ‘Stop’ button, the recording is ended and loaded into an editor window like that depicted in [Figure 3.2.5](#figure-325---mock-up-of-video-gif-capture-video-editing). | P0 |
|11| Alternatively stop the recording and load it into an editor window by pressing the OS level short-cut: Win + Shift + R at any time while recording. | P0 |

#### 3.1.8. Editing

|No. | Requirement | Pri
| - | - | - |
|1 | Load the recording from [section 3.1.7](#317-recording) in an editor window as described in [Figure 3.2.5](#figure-325---mock-up-of-video-gif-capture-video-editing). | P0 |
|2 | A scrub bar should be loaded to trim the recording. Scrubber UI should resemble that of the Photos app in [Figure 1.5.4](#figure-154--trimming-video-via-xbox-game-bar-note-that-the-editing-process-takes-the-user-through-file-explorer-movies--tv-and-photos-before-accessing-the-trimming-functionality). | P0 |
|3 | On the right-hand menu, display a selection menu for either Video or GIF. | P0 |
|4 | Under the ‘Video’ menu, display options to adjust resolution quality, enable/disable system audio, and save the video ([Figure 3.2.5](#figure-325---mock-up-of-video-gif-capture-video-editing)). | P0 |
|5 | Under the ‘GIF’ menu, display options to adjust the resolution, frames-per-second, and save the GIF ([Figure 3.2.6](#figure-326---mock-up-of-video-gif-capture-gif-editing)). | P0 |
|6 | ‘GIF’ menu should allow the user to save the GIF to the clipboard.| P0 |
|7 | The settings icon should display the PowerToys settings menu for VGC when clicked ([Figure 3.2.7](#figure-327---mock-up-of-video-gif-capture-powertoys-settings)). | P0 |

### 3.2. Design Mock-Ups

###### *Figure 3.2.1 - Mock up of Video GIF Capture selection menu*

![SelectionMenu1](./images/GIFSpec/VGCSelect.png "Video GIF Capture selection menu")

###### *Figure 3.2.2 - Mock up of Video GIF Capture expanded selection menu for exact coordinate selection*

![SelectionMenu2](./images/GIFSpec/VGCExpanded.png "Video GIF Capture expanded selection menu")

###### *Figure 3.2.3 - Mock up of Video GIF Capture recording interface prior to recording*

![RecordingMenu1](./images/GIFSpec/VGCRecordPre.png "Video GIF Capture pre-recording menu")

###### *Figure 3.2.4 - Mock up of Video GIF Capture recording interface during recording*

![RecordingMenu2](./images/GIFSpec/VGCRecordPost.png "Video GIF Capture post-recording menu")

###### *Figure 3.2.5 - Mock up of Video GIF Capture video editing*

![EditorVideo](./images/GIFSpec/EditorMenuVideo.png "Video GIF Capture video editing window")

###### *Figure 3.2.6 - Mock up of Video GIF Capture GIF editing*

![EditorGIF](./images/GIFSpec/EditorMenuGIF.png "Video GIF Capture GIF editing window")

###### *Figure 3.2.7 - Mock up of Video GIF Capture PowerToys settings*

![SettingMenu](./images/GIFSpec/VGCSettings.png "Video GIF Capture PowerToys settings")

### 3.3. Open Considerations

* DRM considerations
* Memory considerations when recording
* File size considerations for exporting
* Animated GIF 'copy to clipboard' functionality: Windows currently doesn't support animated GIF copying, so only a static non-animated variant can be stored on the clipboard
* Text overlay functionality
* PowerToys Settings menu options (ex: default encoder, cursor capture, key stroke capture, pre-recording countdown etc.)
* Multi-monitor display behaviors and Multi-DPI compatibility
* OS level shortcuts & hot-keys. Ex: Play, Stop, Pause, Resume, Cancel
* Discoverability of features and settings
* Touch & Pen interaction considerations and supporting UI
* Supported export formats

## 4. Measure Requirements

|No. | Requirement | Implication |Pri. |
| - | - | - | - |
|1 | Total time of recording | Insight into memory requirements for application | P1 |
|2 | # of recordings captured | Information on the frequency of application usage | P1 |
|3 | # of recordings trimmed | Insights into potential editing optimizations | P1 |
|4 | Type of recording zone used | Allows us to recommend defaults to Windows developers | P1 |
|5 | # of times VGC was canceled | Continuous cancellations may imply shortcomings in UX and general usability | P1 |
|6 | % of successful renders | Allows us to track application reliability | P1 |
|7 | Final recording form (GIF vs MP4) | Allows us to track popularity of encoding format to prioritize further improvements and optimizations | P1 |
|8 | Number of times in past 28 days user has engaged with recording tool | Information on whether VGC is being utilized by PowerToys users | P1 |
|9 | Changes to default encoding | Allows us to recommend defaults to Windows developers | P1 |
|10| Size of recording | Insight into memory requirements for application | P1 |

## 5. Dependencies

* Depending on implementation, Snip and Sketch base code for zone selection
* Depending on implementation, Photos app base code for editor trimming
* Depending on implementation, ScreenToGIF as possible OSS base partner
* WinUI 3