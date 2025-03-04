### [VIM](https://www.vim.org/) commands

#### Launch VIM
- Open document
````bash
    vim document
````
- Launch VIM with split window vertically
````bash
    vim -O document_1 document_2
````
- Launch VIM with split window horizontally
````bash
    vim -o document_1 document_2
````
- Launch VIM with tabs
````bash
    vim -p document_1 document_2
````

#### Handle document
- Go to the first line
````bash
    gg
````
- Go to the last line
````bash
    G
````
- Go to the line i
````bash
    iG
    :i
````
- Select string
````bash
    *
````
- Search a string selected
````bash
    n
````
- Undo
````bash
    u
````
- Redo
````bash
    ctrl+r
````

#### Tabs
- Show Tabs
````bash
    :tabs
````
- Create Tab
````bash
    :tabnew
````
- Close current tab
````bash
    :tabclose
````
- Close current tab in `normal mode`
````bash
    ctrl+w c
````
- Move current tab to first
````bash
    :tabm 0
````
- Move current tab to last
````bash
    :tabm
````
- Move current tab to position i+1
````bash
    :tabm {i}
````
- Go to next tab
````bash
    :tabn
````
- Go to previous tab
````bash
    :tabp
````
- Go to first tab
````bash
    :tabfirst
````
- Go to last tab
````bash
    :tablast
````
- Go to next tab in `normal mode`
````bash
    gt
````
- Go to previous tab in `normal mode`
````bash
    gT
````
- Go to tab in position i in `normal mode`
````bash
    {i}gt
````
