=============
PYTHON .VIMRC
=============

VIM Configuration for Python / Cython / C Development.

Keep calm and use VIM!

Requirements
------------

- VIM 7.4
- git
- bash 3.2+

How does it look?
-----------------

.. image:: https://github.com/ets-labs/python-vimrc/wiki/img/screenshot.png

Installation
------------

You can install it by using CLI just have next command executed:

.. code-block:: bash

  sh -c "$(curl -fsSL https://raw.githubusercontent.com/srdjanalea/python-vimrc/master/setup.sh)"

During execution of init script do not worry about error messages. When it
occurs just press enter and wait till all plugins are installed.

Autocompletion
--------------

Current bundle use one of the most comprehensive plugins for autocompletion - 
`Valloric/YouCompleteMe <https://github.com/Valloric/YouCompleteMe>`_.
YouCompleteMe autocompletion plugin requires additional installation that 
depends on environment and functionality you want to have. Detailed 
instructions could be found on plugin page: 
`Valloric/YouCompleteMe <https://github.com/Valloric/YouCompleteMe#installation>`_.


**Note:** Installation for Mac OS with support of clang compiler looks like 
this:

.. code-block:: bash

  ~/.vim/bundle/YouCompleteMe/install.py --clang-completer


To finish command-t module installation do the following:

.. code-block:: bash

   ruby ~/.vim/bundle/command-t/ruby/command-t/ext/command-t/extconf.rb
   cd /home/srdjan/.vim/bundle/command-t/ruby/command-t/ext/command-t/ && make

Key bindings
============

This configuration tends to use standard VIM and installed plugins key 
bindings, but there are some custom key bindings as well:

.. code::

    # Common key bindings:

    inoremap jj     # Esc alternative
    inoremap jk     # Esc alternative
   
    nmap <C-t>      # Toggle Command-T search
    nmap <C-b>      # Toggle Command-T buffer search 
    nmap <C-j>      # Toggle Co
    nmap <F8>       # Toggle NERDTree buffer 
    nmap <F9>       # Jump to the previous buffer
    nmap <F10>      # Jump to the next buffer
    
    nmap <leader>q  # Delete buffer

    # Python mode key bindings:

    let g:pymode_doc_key='K'
    let g:pymode_breakpoint_key='<leader>b'
    let g:pymode_run_bind='<F5>'

    nmap <leader>g :YcmCompleter GoTo<CR>
    nmap <leader>d :YcmCompleter GoToDefinition<CR>
