# runin
Launch a terminal to run a command, passing on stdin and stdout

```
runin [-h, --help] TERMINAL COMMAND...

Run COMMAND... in the specified TERMINAL, while preserving pipes for COMMAND

    -h, --help  show this help text
```
This allows piping through programs that require a terminal. An example usecase would be using [`fzf`](https://github.com/junegunn/fzf) in the terminal [`alacritty`](https://github.com/alacritty/alacritty) as a [`dmenu`](https://wiki.archlinux.org/index.php/Dmenu) replacement.

To pick a one of file1, file2, file3 to open in gedit:  
`echo -e "file1 \n file2 \n file3" | runin alacritty fzf | xargs gedit`

More advanced examples can be found in my [`sway` dotfiles](https://github.com/nichobi/dotfiles/blob/db19a1f1748d89ddd9ac0507bd604b58306edaaf/sway/config#L19)
