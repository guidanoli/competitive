# Competitive Programming Toolkit

## Description

A toolkit for language-agnostic competitive programming, focused on _POSIX_ systems.

## Motivation

Even though C and C++ dominate the competitive programming ecosystem, it's not hard to spot some submissions using Python, Perl and Java, for instance.
That's because every language has its pros and cons, so knowing many different languages can not only make you a better programmer but also a better competitor.

The problem is: keeping a polyglot development environment consistent and tidy is oftentimes harder than it may seem.
What this toolkit promotes is an abstraction for developing with different programming languages at once. You can think of it as the console interface of a very simple integrated development environment.

## Mechanism

The user accesses the toolkit by calling the `cptk` script and passing it any of the available commands, such as `init` for setting the current language.

## Dependencies

Apart from [bash], different sets of dependencies are required for running and debugging programs of each language.
Since you'll most likely be working with only a portion of them, the following table is there to help you determine which software you actually need.

| Programming Language | Label | Running | Debugging |
| :- | :- | :- | :- |
| C | `c` | [gcc], [make] | [gdb] |
| C++ | `cpp` | [g++], [make] | [gdb] |
| C# | `cs` | [mcs], [make] | [gdb] [(1)] |
| Go | `go` | [go], [make] | [gdb] [(2)] |
| Haskell | `haskell` | [ghc], [make] | [gdb] [(4)] |
| Java | `java` | [javac], [java], [make] | [jdb] |
| Javascript | `js` | [node] | |
| Kotlin | `kotlin` | [konanc], [make] | [gdb] [(5)] |
| Pascal | `pascal` | [fpc], [make] | [gdb] [(3)] |
| Perl | `perl` | [perl] | |
| Python | `python` | [python] | |
| Ruby | `ruby` | [ruby] | |

Some commands require additional software too:

| Command | Dependencies |
| :- | :- |
| edit | [vi] |
| copy | [clip.exe], [xclip] or [pbcopy] |
| paste | [powershell.exe], [xclip] or [pbpaste] |

## Setup

1. **Check out this repository where you want it installed**. A good place is `~/.cptk` (but you could install it anywhere else).

```sh
git clone https://github.com/guidanoli/cptk.git ~/.cptk
```

2. **Edit your shell profile if you want to access the `cptk` command-line utility**. You can replace `cpp` with any other programming language of your liking.

```sh
echo 'export PATH=$PATH:$HOME/.cptk/bin' >> ~/.bashrc
echo 'cptk init cpp' >> ~/.bashrc
```

## Usage

Run `cptk --help` for usage information.

## Tests

After installing all the dependencies, you can run `tests/all`.

[(1)]: https://www.mono-project.com/docs/debug+profile/debug/#debugging-with-gdb
[(2)]: https://golang.org/doc/gdb
[(3)]: https://www.freepascal.org/docs-html/user/userse54.html#x165-17200010.2
[(4)]: https://downloads.haskell.org/~ghc/latest/docs/html/users_guide/debug-info.html
[(5)]: https://kotlinlang.org/docs/reference/native/debugging.html
[bash]: https://www.gnu.org/software/bash/
[clip.exe]: https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/clip 
[fpc]: https://www.freepascal.org/
[g++]: https://gcc.gnu.org/
[gcc]: https://gcc.gnu.org/
[gdb]: https://www.gnu.org/software/gdb/
[ghc]: https://www.haskell.org/ghc/
[go]: https://golang.org/
[java]: https://docs.oracle.com/javase/7/docs/technotes/tools/windows/java.html
[javac]: https://docs.oracle.com/javase/7/docs/technotes/tools/windows/javac.html
[jdb]: https://docs.oracle.com/javase/7/docs/technotes/tools/windows/jdb.htm
[konanc]: https://github.com/JetBrains/kotlin-native
[make]: https://www.gnu.org/software/make/
[mcs]: https://www.mono-project.com/
[node]: https://nodejs.org/en/
[pbcopy]: http://mirror.informatimago.com/next/developer.apple.com/documentation/Darwin/Reference/ManPages/man1/pbcopy.1.html
[pbpaste]: http://mirror.informatimago.com/next/developer.apple.com/documentation/Darwin/Reference/ManPages/man1/pbpaste.1.html
[perl]: https://www.perl.org/
[powershell.exe]: https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/powershell
[python]: https://www.python.org/
[ruby]: https://www.ruby-lang.org/en/
[vi]: http://ex-vi.sourceforge.net/
[xclip]: https://github.com/astrand/xclip
