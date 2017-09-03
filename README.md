# vim-trimswap

Remove redundant Vim swap files from the Vim swap directory.
If you do not use a single central swap directory for Vim, vim-trimswap is not for you.

For each Vim swap file currently not in use and containing no changes in comparison to the original, manually saved file, vim-trimswap will remove the swap file.

vim-trimswap relies on Vim to detect the inactive and unmodified swap files.
Vim makes mistakes.
There are at least some false negatives, e.g. swap files that would be safe to remove but are falsely detected to be handled by a still-running process.
I have not yet seen false positives but your mileage may vary.

vim-trimswap relies on the output of `vim -r` to be in English and in UTF-8.

## Usage

Run `vim-trimswap` to remove redundant Vim swap files.
