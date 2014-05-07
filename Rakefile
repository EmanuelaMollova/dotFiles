#TODO check if  symlinks already exist...

require 'fileutils'
include FileUtils

desc "Configure bash"
task :configure_bash do
  puts 'Configuring bash'

  system 'ln -s ~/dotFiles/bash $HOME/.bash'
  system 'ln -s ~/dotFiles/bash/bashrc $HOME/.bashrc'
end

desc "Install zsh and oh-my-zsh"
task :install_zsh do
  puts 'Installing zsh'

  #TODO solarized + modified powerline font
end

desc "Configure zsh"
task :configure_zsh do
  puts 'Configuring zsh'

  system 'cp ~/dotFiles/zsh/oh-my-zsh/themes/agnoster_.zsh-theme $HOME/.oh-my-zsh/themes/agnoster_.zsh-theme'
  system 'ln -s ~/dotFiles/zsh/zshrc $HOME/.zshrc'
  system 'ln -s ~/dotFiles/zsh/zprofile $HOME/.zprofile'
end

desc "Install Vim and gVim"
task :install_vim do
  puts 'Installing Vim'
  system 'sudo apt-get install vim'

  puts 'Installing gVim'
  system 'sudo apt-get install vim-gtk'
  #TODO ctags
end

desc "Configure Vim"
task :configure_vim do
  puts 'Configuring Vim'

  system 'git clone https://github.com/gmarik/Vundle.vim.git ~/dotFiles/vim/bundle/Vundle.vim'
  system 'ln -s ~/dotFiles/vim $HOME/.vim'
  system 'ln -s ~/dotFiles/vim/vimrc $HOME/.vimrc'
  system 'vim +PluginInstall +qall'
end

desc "Install Git"
task :install_git do
  puts "Installing git"
  system 'sudo apt-get install git'
end

desc "Configure Git"
task :configure_git do
  puts 'Configuring Git'
  system 'ln -s ~/dotFiles/git/gitconfig $HOME/.gitconfig'
end
