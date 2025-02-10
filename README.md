# Meow Universal Recovery Project
Main repository for the manifest files used to get the Meow Universal Recovery Project sources.

> [!NOTE]
> Make sure you have enough space to store MURP source code.

## Getting Started
First, create new folder and cd to it:<br>
`mkdir MURP && cd MURP`<br>
Then, sync source code:<br>
`repo init --depth=1 -u https://github.com/Meow-Universal-Recovery-Project/manifest.git -b main`<br>
`repo sync -jX`<br>
After that, apply patch:<br>
`patch -p1 < miscellaneous/patches/12.1.diff`<br>

