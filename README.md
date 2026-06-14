# VimFuck

A Brainfuck interpreter written entirely in Vim macros. Yes, really. No plugins,
no dependencies, just Vim doing something it was never meant to do :)

I built this because someone said "you can't" and I had a free weekend. Turns out
Vim's macro engine is Turing-complete enough to run another Turing-complete language,
which feels illegal but isn't.

## Install

```bash
curl -L https://raw.githubusercontent.com/1611Dhruv/VimFuck/main/vimfuck.vim -o vimfuck.vim
```

Windows folks, swap that for `Invoke-WebRequest`. You know who you are.

## Run

Open your `.bf` file in Vim, then:

```
:source vimfuck.vim
:call Vimfuck()
```

- Ignore the errors it throws on setup. Known bug, it's fine, it's a vibe.
- If your program reads input, type it and hit `@c`
- When you're done, `@z` cleans up after itself (more than I can say for me)

## Example

Hello World, the hard way:

```brainfuck
++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.
```

## See It In Action

https://github.com/user-attachments/assets/132e79cd-73fe-4b6c-b30b-c5822f4feacb

https://github.com/user-attachments/assets/67e953f5-85cb-4cbc-a47e-ba1e3dff6ec6


## License

MIT. Do whatever, just don't blame me when your editor becomes self-aware.

 \\\( ﾟ◡ﾟ)/
