# vim-trimswap

Remove redundant Vim swap files from the swap directory.

vim-trimswap will remove each swap file that contains no changes in comparison to the original, manually saved file and that is not in use by a running process.


## Assumptions for correct behavior

- Vim uses only one directory for swap files, e.g. with `set directory=~/.vim/swap//` in vimrc.
- The output of `vim -r` is in English and in UTF-8.
- `vim -r` does not detect modified swap files as unmodified.
- `vim -r` does not detect active swap files as inactive.
    - It does happen that swap files are falsely detected to be handled by a running process, though. That is why vim-trimswap might not remove all expected files.


## Usage

Run `vim-trimswap` to remove redundant swap files.
