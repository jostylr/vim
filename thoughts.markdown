# First steps into Vim

Inspired by DailyJS's comment about Vim in relation to Atom, I decided to delve into Vim. 

So far, I have: 

1. Used the default Vim on my Mac.
2. Worked through Vim Tutor, about an hour or two.
3. Read throught the first 12 sections of the user manual. This by far the most I have ever read of any manual. 
4. Learned from [codeography](http://www.codeography.com/2013/06/26/remapping-caps-lock-was-only-the-beginning.html) that I can map the Caps Lock to control for combo keys, but escape for isolated presses. I also set the right command key to be an enter on single press. Not used to that yet. It uses the software [KeyRemap4MacBook](https://pqrs.org/macosx/keyremap4macbook/index.html.en)
5. Started this journal.

I need to get my head around how to set it up for my workflow. For awhile, this is going to be a bit painful. I can see how incredibly powerful this tool is, but I have muscle memory to forget. 

As with any tool, why am I switching? Basically, I have been using Sublime and I just never got into all of its powers. I am not sure if there was anything wrong with it, but I feel more comfortable in investing a lot of time and energy learning a program that has been used for decades by power users in my area of interest. I know that if I master Vim, it will always be available and it will do anything I want it to do. I am not sure the same can be saif for all these other fly-by-night editors. 

Having said that, let me go install some recently created plugins... 

* [Vundle](https://github.com/gmarik/Vundle.vim)   A nice [Vundle vs Pathogen story](http://jameslaicreative.com/moving-up-upgrading-from-pathogen-to-vundle/) 
* Git:  Fugitive
* Markdown:  [Voom](https://github.com/vim-voom/VOoM) which does outlining
* [vim-markdown](https://github.com/tpope/vim-markdown) which does github fence highlighting. A little bit of info at [Coderwall](https://coderwall.com/p/ftqcla)

## Commands to use

* Change directory by `:lcd dir` The lcd makes it local to the window. Thus, if you have multiple windows, you can work with multiple projects in each window.
* More [tips](http://stackoverflow.com/questions/1276403/simple-vim-commands-you-wish-youd-known-earlier) including ctrl-q to select rectangle, shift-v to select rows, v to go into vi mode. 
* [Selecting pasted text](http://usevim.com/2014/02/14/selecting-put-text/)


# Setup in Vimrc

* Set autoindent to on to just have indentation follow from line to line. Use CTRL-D to unindent a line. 
* The following commands can be used to make sure one uses spaces instead of tabs: 
    set smartindent
    set tabstop=4
    set shiftwidth=4
    set expandtab
* Paste with appropriate indentation: ? [SO](http://stackoverflow.com/questions/2514445/turning-off-auto-indent-when-pasting-text-into-vim)
* :noh will remove the highlighting that happens with a search
* Start two files in vertical split with   `vim -O file1 file2`
* [Cheat Sheet](http://bullium.com/support/vim.html)
* Searching for visually selected text [using `*`: ](http://vim.wikia.com/wiki/Search_for_visually_selected_text)
* [Status Line](http://stackoverflow.com/questions/5375240/a-more-useful-statusline-in-vim) and  %{fugitive#statusline()} from fugitive
* :set linebreak will wrap text in between words, then :set showbreak=>\ with a space after the slash will do a nice indent view. 
* set dir=~/.vim/swp to keep the swap files from polluting directories.
* set ww=<,>,[,]  to enable wrapping around when using cursor keys. do not use that with h and l because of the d3h kind of command which would then delete more than intended. I think. 

## MacVim

I really wanted the Cmd-S save functionality. So after pulling my hair out trying to get it to work in iterm2, I installed MacVim. 

