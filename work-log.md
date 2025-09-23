# This file records raw thoughts, tasks, changes, and progress
## How I see the program functioning
- `ruderb` with a path will just create a feed in the path (`ruderb create`)
- `ruderb` with nothing ~~should show help~~ should just create a feed in the current folder if there are any audio files in there
- `ruderb create` should do the same as above: take the files in the current folder and create a feed according to defaults
- Empty, the site defaults to `http://localhost/audio-files-folder/feed-name.xml`
- Command line flags, that'll let me set site and path. (the final part of the path will always be the folder name)
    - for example: `http://localhost/fiction/audio-files-folder/feed-name.xml`
    - only one level for now. site -> category -> book-folder
- A config file, (yaml/env) that will hold defaults? or multiple choices?
    - go create --category=fiction will use fiction category in the url?
    - config file will also hold settings for feed, such as author, email, and site url


## Tasks as I see them
- [ ] Learn how pull requests work in go land
- [ ] Find dependencies, like I use in Python / Go  
      - viper(MIT)=[config](https://crates.io/crates/config) MIT  
      - cobra command line framework=[clap](https://crates.io/crates/clap) MIT  
      - dhowden/tag(BSD-2)=[audiotags](https://crates.io/crates/audiotags) MIT
      - gorilla/feeds(BSD-3)=[feed-rs](https://crates.io/crates/feed-rs)  
      - goreleaser=[cargo-dist](https://crates.io/crates/cargo-dist) MIT goreleaser might also do it for rust  
- [ ] Update Project LICENSE once I figure out above (BSD 2 Clause)
- [ ] Learn the basic rust toolchain. does not have to be perfect. Learn industry standards later. Right now I desperately need derb to work on the Pi
- [ ] Figure out how to read in environment variables from a .env file
- [ ] Figure out to read metadata from audio files
- [ ] Change the whole project into a clap app
- [ ] Create an app that just saves config
- [ ] Get path from command line
- [ ] verify path,
- [ ] get stem from path and tag to feed url
- [ ] split path to get end folder to tag on to url
- [ ] and prints things out
- [ ] figure out how to read in the contents of a directory and print filenames to screen
- [ ] figure out how to import a tag package and get it to read the filenames you give it and print out the metadata it gets
- [ ] Figure out how to write images from metadata to disk
- [ ] Write slowly. Learn how types work as you go.
- [ ] Learn how to create a feed
- [ ] Accept any folder, read the files in there and then write the feed back in there
- [ ] check only for audio files and print those
- [ ] print them sorted? so i can pass them along in that order to the rss library
- [ ] do we need to sort by filename? or track num? figure that out. *(Narrator: we used track numbers)*
- [ ] Create a feed
- [ ] First run!
- [ ] Learn how github releases work, so I can distribute stuff
- [ ] if there is a cover, leave it alone
- [ ] handle conditions when there is no cover image in the audiofile itself
- [ ] try moving to the ffmpeg c library
- [ ] Add sample config file and include instructions on placement
- [ ] Integrate feedback from friends and family
- [ ] a `ruderb init` command that creates a new config file in the current folder? or saves to `~/.config/ruderb/ruderb.yaml`
- [ ] Tests

---
