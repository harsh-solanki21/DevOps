# Vim Commands

`:wq` - save and quit
`:q!` - quit without save
`u` - undo
`3u` - to go back 3 undos
`ctrl + r` - redo
`:5` - to go to line number 5
`gg` - to jump to the start of file
`G / :$` - to jump to the end of file
`e` - to go to the end of word
`0` - to jump to the beginning of line
`$` - to jump to the end of line

`v` - to go into visual mode
`d` - to delete selected
`dd` - to delete entire line
`D` - to delete rest of the line after cursor
`y` - copy selected text
`p` - paste copied text
`5p` - paste copied text 5 times
`yiw` - to yank (copy) inner word
`yi"` - to yank (copy) inner quotations

`w` - to jump to the next word
`b` - to jump to the previous word
`dw` - to delete a word
`d2w` - to delete 2 words
`5d2w` - 5 times delete 2 words
`d2b` - to delete 2 words backwards
`diw` - to delete the word you're in
`d$` - delete till the end of line
`di"` - delete inner quotations
`di(` - delete inner parenthesis
`yt{` - yank till {

`%` - to jump to opening/closing bracket
`d%` - delete everything in between that brackets
`f*` - to find the position of next \* and jump to it

`:split fileName` - horizontally splits windows
`:vsplit fileName` - vertically splits windows
