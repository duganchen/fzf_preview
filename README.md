# FZF Previewer

A previewer for FZF.

Note that the current implementation does *not* support terminals other than Kitty and Ghostty.

Copy the scripts to a directory on your PATH.

Set either Ranger's scope.sh or the pistol project as the fallback previewer, the same way you would in nnn.
The process consists of installing either or both into your PATH, and then setting either NNN_PISTOL or NNN_SCOPE to 1. See:

https://github.com/jarun/nnn/blob/master/plugins/preview-tabbed

To test, put a still image, a movie, and a file of another type, into a directory. Then cd to that directory and do:

    find . -type f -maxdepth 1 | fzf --preview='fzf_preview {}'

You should have image previews for the movie and still image, and a normal preview for the third file.

## Use Cases

These are some of the uses I've found for it:

* [DOS games](./dosgames/README.md)
* [TV episodes](./episodes/README.md)

## Note:

I'm running Ghostty with FISH on Fedora, and that's what this is coded for. Expanding this to support
other terminals is left as an exercise for the community contributors. Hint: look at the fzf_*_image scripts.

Thumbnails are cached in ~/.cache/fzf_thumbnails.

Heavily inspired by this project:

https://github.com/gmou3/fzf-preview/

I think it's worth mentioning that this is actually my second thumbnailer project. My first was:

https://github.com/duganchen/kitty-pistol-previewer
