# Lecture Studio Open-Source Notices

Lecture Studio includes, installs, or interoperates with third-party open-source software. Lecture Studio's proprietary license does not replace or restrict the licenses of these components.

This notice lists the components Lecture Studio uses directly, plus the packages those components pull in during first-time setup. Versions below match the pins in the setup script. Before each public release, build the runtime in a clean location, save the exact package inventory, and confirm the license of every item (see "Release checklist").

## Components shipped inside the app

### Sparkle 2

Website: https://sparkle-project.org/
Source: https://github.com/sparkle-project/Sparkle
License: MIT, with additional third-party notices in Sparkle's LICENSE file
License text: https://github.com/sparkle-project/Sparkle/blob/2.x/LICENSE

Copyright (c) 2006-2013 Andy Matuschak.
Copyright (c) 2009-2013 Elgato Systems GmbH.
Copyright (c) 2011-2014 Kornel Lesiński.
Copyright (c) 2015-2017 Mayur Pawashe.
Copyright (c) 2014 C.W. Betts.
Copyright (c) 2014 Petroules Corporation.
Copyright (c) 2014 Big Nerd Ranch.

The complete Sparkle license, including its bundled external notices, must remain available with Lecture Studio's distribution.

## Components downloaded during first-time setup

Lecture Studio does not ship these. The setup screen downloads them to the user's Mac into a private folder.

### Python 3.12 (via uv)

License: Python Software Foundation License
Source: https://www.python.org/

### uv 0.12.17

Source: https://github.com/astral-sh/uv
License: MIT OR Apache-2.0
License files: https://github.com/astral-sh/uv/blob/main/LICENSE-MIT and https://github.com/astral-sh/uv/blob/main/LICENSE-APACHE

Copyright (c) 2025 Astral Software Inc.

Lecture Studio uses uv under the MIT license reproduced below. The download is verified against a pinned SHA-256 checksum.

### MLX 0.32.2 (and mlx-metal)

Source: https://github.com/ml-explore/mlx
License: MIT

Copyright © 2023 Apple Inc.

On macOS, MLX installs its companion `mlx-metal` package at the same version, which carries the same license.

### MLX Whisper 0.4.3 / MLX Examples

Source: https://github.com/ml-explore/mlx-examples/tree/main/whisper
License: MIT

Copyright © 2023 Apple Inc.

### imageio-ffmpeg 0.6.0

Source: https://github.com/imageio/imageio-ffmpeg
License: BSD 2-Clause (see below)

Copyright (c) 2019-2025, imageio. All rights reserved.

### FFmpeg

Website and source: https://ffmpeg.org/
Legal information: https://ffmpeg.org/legal.html

Lecture Studio uses the FFmpeg executable bundled inside the imageio-ffmpeg package for audio decoding and silence detection. Pre-built FFmpeg binaries are commonly compiled with GPL-licensed options enabled, so this binary may be governed by GPL terms rather than LGPL terms. The exact license and build configuration of the shipped binary must be confirmed for each release (for example, by running the binary with `-version` and `-L`). If GPL applies, the corresponding source offer and license notice requirements must be honored.

Lecture Studio runs FFmpeg as a separate program and does not link it into the app.

### Whisper models

OpenAI Whisper source: https://github.com/openai/whisper
Model repositories used by Lecture Studio:

- https://huggingface.co/mlx-community/whisper-large-v3-turbo (default, "turbo")
- https://huggingface.co/mlx-community/whisper-large-v3-mlx ("large")

These are MLX conversions of OpenAI's Whisper models. Whisper is released under the MIT license, but each model repository may carry its own license and notices. Verify and retain the license for each exact model revision before release. Models are downloaded on first use and are not bundled with the app.

## Packages installed alongside MLX Whisper

MLX Whisper 0.4.3 requires the packages below. Each remains governed by its own license, and each of these installs further dependencies of its own. The licenses listed are the ones expected for these packages and must be verified against the installed versions before release.

| Package | Expected license |
| --- | --- |
| numpy | BSD 3-Clause |
| scipy | BSD 3-Clause |
| torch | BSD 3-Clause (bundles additional third-party notices) |
| numba (and llvmlite) | BSD 2-Clause (llvmlite includes LLVM under Apache-2.0 with LLVM exceptions) |
| tiktoken | MIT |
| huggingface_hub | Apache-2.0 |
| tqdm | MPL-2.0 AND MIT |
| more-itertools | MIT |

Apache-2.0 and MPL-2.0 components require that a copy of their license accompany distribution. If these packages are only downloaded by the user's own Mac at setup time, confirm with the release checklist how and where their license files are made available.

## What Lecture Studio does not include

- AI study features send text to OpenAI or Anthropic using the user's own API key. These are third-party services under their own terms and are not open-source components.
- Lecture Studio Plus licensing and purchase flows are handled by a separate service and are not covered here.

## MIT License text

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## BSD 2-Clause License — imageio-ffmpeg

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice,
   this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## Release checklist

1. Build the runtime in a clean location and save the exact package inventory:

   ```bash
   /path/to/runtime/venv/bin/python -m pip freeze > THIRD_PARTY_VERSIONS.txt
   ```

2. Review that inventory against the table above and add any package or notice that is missing. `pip freeze` lists versions only, not licenses.
3. Check the FFmpeg binary's license and build configuration, and honor any GPL obligations.
4. Check the license of each Whisper model revision.
5. Confirm Sparkle's full license text ships with the app. The Sparkle.framework in the 1.0.7 build does not include a LICENSE file, and the app links to this notice on GitHub instead.
6. Keep this file at the GitHub path the app links to: `OPEN_SOURCE_NOTICES.md` on the `main` branch.

This notice is an inventory and a checklist, not legal advice.
