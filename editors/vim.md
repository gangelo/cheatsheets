# Vim

## Some helpful vim commands/shortcuts
    
    y -> copy
    d -> cut/delete
    p -> paste

    CTRL+N -> cycles words forward
    CTRL+P -> cycles words backward
    CTRL+X CTRL+L -> cycles lines

## Motion: http://vimdoc.sourceforge.net/htmldoc/motion.html

The motion commands can be used after an operator command, to have the command operate on the text that was moved over. That is the text between the cursor position before and after the motion. Operators are generally used to delete or change text. The following operators are available:

    |c| c   change
    |d| d   delete
    |y| y   yank into register (does not change the text)
    |~| ~   swap case (only if 'tildeop' is set)
    |g~|    g~  swap case
    |gu|    gu  make lowercase
    |gU|    gU  make uppercase
    |!| !   filter through an external program
    |=| =   filter through 'equalprg' or C-indenting if empty
    |gq|    gq  text formatting
    |g?|    g?  ROT13 encoding
    |>| >   shift right
    |<| <   shift left
    |zf|    zf  define a fold
    |g@|    g@ call function set with the 'operatorfunc' option

## Basic moving
    
    h -> left
    l -> right
    j -> up line
    k -> down line
    e -> forward to end of word
    w -> forward to begin of word
    b -> backward to begin of word
    0 -> start of line
    $ -> end of line
    gg -> start of file
    G -> end of file
    H -> start of screen
    L -> end of screen
    M -> middle of screen
    ^ -> first no-blank char of line
    g_ -> last no-blank char of line
    g0 -> start of line (wrap-wise)
    g$ -> end of line (wrap-wise)
    gm -> middle of line (wrap-wise)
    | -> move to col (better used with a number, like g does for line)
    f{char} -> [count] occurrence of {char} to the right
    F{char} -> [count] occurrence of {char} to the left
    t{char} -> like f, but stops before
    T{char} -> like F, but stops after
    ; -> repeat last f, F, t, T [count] times
    , -> repeat last f, F, t, T [count] times in the opposite direction
    ( -> [count] sentences backward
    ) -> [count] sentences forward
    { -> [count] paragraph backward
    } -> [count] paragraph forward
    % -> to matching ([{<>}])


 ## v -> selects text (the following modifiers apply)
 
    a -> selects delimiters (like <{[("''")]}>)
    i -> selects only content
    for the two above:
        w -> selects word
        s -> selects sentence
        p -> selects paragraph
        [ -> a [ block
        { -> a { block
        ( -> a ( block
        < -> a < block
        " -> a quote
        ' -> a quote
        ` -> a quote

Of course, the above can also be used with stuff like delete (d); dd deletes only the current line.
