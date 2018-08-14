### VIM commands

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
- Go to previous tab in normal mode
````bash
    gT
````
- Go to tab in position i in normal mode
````bash
    {i}gt
````