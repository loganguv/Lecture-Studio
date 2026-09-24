# Lecture Studio Open-Source Notices

Lecture Studio includes, installs, or interoperates with third-party open-source software. Lecture Studio's proprietary license does not replace or restrict the licenses of these components.

This notice reflects the known direct components used by the current source. Python packages may install additional transitive dependencies. Before each public release, generate and review a complete dependency inventory from the release runtime and retain all required license files.

## Direct components

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

### uv 0.12.17

Source: https://github.com/astral-sh/uv  
License: MIT OR Apache-2.0  
License files: https://github.com/astral-sh/uv/blob/main/LICENSE-MIT and https://github.com/astral-sh/uv/blob/main/LICENSE-APACHE

Copyright (c) 2025 Astral Software Inc.

Lecture Studio may use uv under the MIT license reproduced below.

### MLX 0.32.2

Source: https://github.com/ml-explore/mlx  
License: MIT

Copyright © 2023 Apple Inc.

### MLX Whisper 0.4.3 / MLX Examples

Source: https://github.com/ml-explore/mlx-examples/tree/main/whisper  
License: MIT

Copyright © 2023 Apple Inc.

### imageio-ffmpeg 0.6.0

Source: https://github.com/imageio/imageio-ffmpeg  
License: BSD 2-Clause

Copyright (c) 2019-2025, imageio. All rights reserved.

### FFmpeg

Website and source: https://ffmpeg.org/  
Legal information: https://ffmpeg.org/legal.html

FFmpeg is generally available under LGPL 2.1 or later, but particular binaries can be governed by GPL terms depending on enabled build options. Lecture Studio obtains an FFmpeg executable through imageio-ffmpeg. The exact binary license and configuration must be verified for each shipped runtime. Corresponding-source and relinking obligations, when applicable, must be honored.

### Whisper models

OpenAI Whisper source: https://github.com/openai/whisper  
Model repositories used by Lecture Studio:

- https://huggingface.co/mlx-community/whisper-large-v3-turbo
- https://huggingface.co/mlx-community/whisper-large-v3-mlx

Model cards and repository files may carry their own licenses and notices. Verify and retain the license applicable to each exact model revision before release.

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

## Python and transitive packages

The private runtime uses Python 3.12 and packages installed from Python package indexes. Python is distributed under the Python Software Foundation License. Each installed package remains governed by its own license.

Before release, build the runtime in a clean location and save an exact package inventory, for example:

```bash
/path/to/runtime/venv/bin/python -m pip freeze > THIRD_PARTY_VERSIONS.txt
```

Review that inventory and add all required copyright and license notices. `pip freeze` is an inventory aid, not a complete license report.
