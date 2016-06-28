# About

This is a fork of the VimBlog project, located at: https://github.com/danielmiessler/VimBlog

And VimBlog was a fork of the VimRepress project, located at: https://github.com/vim-scripts/VimRepress

VimWordpress is a Python 3 plugin for Vim to manage Wordpress (incl. wordpress.com) blogs. As of 2016, other vim plugins lack the support of Python 3, which motivates the development of the VimWordpress plugin.

## Requirements

- Vim 7.3+ with Python 3 support (Python 2 support is dropped) 
- Python 3 Environment matched wtih Vim's support ("has(python3)" return 1 in vim)
- python-markdown/python-markdown2 installed (execute "pip install markdown2" in shell)
- Wordpress 3.0.0 +

## Installation

1. Use Vundle to add mrpeterlee/VimWordpress to the Plugin source.
    Plugin 'mrpeterlee/VimWordpress'
2. Create a ~/.vimpressrc file, and put the following in it

<code>
    [Blog0]
    blog_url = https://yoursite.com/ 
    username = your_user_name
    password = your_password
</code>

## Command Examples

Some commands list above contain special usage, example below may clearify them for you. 

    :BlogList             -  List 30 recent posts. 
    :BlogList page        -  List 30 recent pages. 
    :BlogList post 100    -  List 100 recent posts. 

    :BlogNew post         -  Write an new post. 
    :BlogNew page         -  Write an new page. 

    :BlogSave             -  Save (defautely published.) 
    :BlogSave draft       -  Save as draft. 

    :BlogPreview local    -  Preview page/post locally in your browser. 
    :BlogPreview publish  -  Same as `:BlogSave publish' with brower opened. 

    :BlogOpen 679 
    :BlogOpen http://your-first-blog.com/archives/679 
    :BlogOpen http://your-second-blog.com/?p=679 
    :BlogOpen http://your-third-blog.com/with-your-custom-permalink 

## Commands

A few shortcuts was recommended in VimBlog for day-to-day blogging:

### Starting workflow

From the shell I launch these two character shortcuts to begin blogging immediately.

-  <code>alias nb="vim +BlogNew</code>
-  <code>alias eb="vim +BlogList</code>

### Inside Vim

Once inside Vim I can run these.

-  <code>nnoremap <leader>b :BlogSave publish<CR></code>
-  <code>nnoremap <leader>h :set ft=HTML<CR><CR></code>

### Credits

All credit to Pentie for creating VimRepress, which this is based on.
