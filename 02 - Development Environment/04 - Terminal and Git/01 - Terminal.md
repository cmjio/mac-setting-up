# Terminal setup

## Installing iTerm 2

Go to [iTerm 2 > Home](http://www.iterm2.com/#/section/home) and download the latest version that you find, even if it's in beta, trust me.

Once downloaded, simply drag it to your Applications folder, and start using it.

To use Zsh simply run the following commands and open a new shell:<br />
`$ chsh -s /bin/zsh`<br />
`$ sudo chsh -s /bin/zsh`

## Installing the Solarized color scheme

Go to [GitHub > altercation/solarized > iterm2-colors-solarized](https://github.com/altercation/solarized/tree/master/iterm2-colors-solarized) and download it whichever way you can, then simply drag it on top of your iTerm 2 application icon and it will be installed. To use it go to *Preferences > Profiles > Colors* and click "Load Presets..." and load the Solarized preset.

# Installing Homebrew

## Obtaining Xcode Command Line Tools

Go to [Apple Developer](https://developer.apple.com/downloads) and download the Command Line Tools. Once downloaded, install them.

Also remember to download the full Xcode, as some do require it: [Apple > iTunes > AppStore > Xcode](https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12)

Remember to open Xcode and allow it to install itself, otherwise you will get an error regarding it's license.

## Installing Homebrew

Simply run the following command in the Terminal application:<br />
`ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"`

After that does what it should, simply run the following command:<br />
`brew doctor`

And fix any problems it shows, if it shows any.

Now you can install whatever you want.

# Installing things with Homebrew

`$ brew install ack`<br />
`$ brew install par`<br />
`$ brew install tmux`<br />
`$ brew install reattach-to-user-namespace`