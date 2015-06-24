# pathogen.sh

Relatively basic bash script to allow one to install Vim plugins from the
command line using tpope's [pathogen.vim](https://www.github.com/tpope/vim-pathogen), adding the plugins as submodules. Also allows complete removal of
submodules.

## Install

1. Put `pathogen` somewhere in `$PATH`
2. (Optional) Add `$SHELL.completion` somewhere it will get sourced


## Usage

`pathogen.sh` is pretty simple to use, much like `pathogen.vim`, it provides 2
commands, install and remove.

Due to the sheer scale of how you can use
`pathogen install`, there's no completion for it, but `pathogen remove` is
capable of detecting all plugins configured *using this method*.

**Any plugins not configured as submodules will not show up in completion.**

### Examples
`pathogen install <site>://<user>/<repo>`

Uses a custom url scheme to complete `<site>` to its value in `$SITES`. Feel
free to add your own, I only thought of those two.

`pathogen install <user>/<repo>`

Defaults to github, as it's the most commonly used platform.

`pathogen install <repo>`

Defaults to github, and uses `$USER` to allow you to easily clone your own
plugins, assuming you have the correct setup in `$HOME/.gitconfig`.

`pathogen remove <repo>`

Either manually or tab-completed, removes and cleans up `<repo>`.


## License

Copyright (c) 2015, Ellis Kenyo
All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
    this list of conditions and the following disclaimer in the documentation
    and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
    contributors may be used to endorse or promote products derived from
    this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS
IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
