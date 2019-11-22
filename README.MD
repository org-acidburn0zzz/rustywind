## What

Inspired by [Ryan Heybourn's](https://github.com/heybourn) [headwind](https://github.com/heybourn/headwind)
vscode plugin. This is a CLI tool that will look through your project and sort all [Tailwind CSS](https://tailwindcss.com) classes. It will also delete any
duplicate classes it finds

## Why?
When Ryan released his vscode extension some people expressed an interest in having a CLI version. 

In addition, I've had an interest in learning rust. I usually learn by doing. I thought this would be
the perfect opportunity to make a small useful tool while learning rust. 

Keep in mind this is my first rust project. My code here is most likely going to be ugly and not idiomatic rust.
If you are a rust expert you're help in making the code nicer and more idiomatic will be greatly appreciated.

Any and all feedback and criticism is very welcome. If im doing anything stupid please let me know.

## The Plan

### MVP
1. Get a list of all files in current directory recursively. 
2. Ignore all files in .gitignore
3. Get all contents from the list of files 1 by 1
4. Run regex on all file contents, and save files
5. Release

### Phase 2 (CLI)
1. Add CLI parser
2. Use CLI parser to choose directory or file to run on
3. Add `--dry-run` option that shows which files it will run on
4. Add `--write` option which will change the files, change default to printing results to the terminal
5. Add ability to exclude folders, or files using regex pattern
6. Add argument for only searching in certain file types

### Phase 3 (Performance)
1. Search and change files in parallel (parallel map?)

### Later Possibilities...
* Add ability to add custom sorter
* Derive sorter from evaluation generated CSS from tailwind config file