task :configure_bash do
  create_symlink('.bashrc', 'bash/bashrc')
  create_symlink('.bash', 'bash')
end

task :configure_zsh do
  system 'cp ~/dotFiles/zsh/oh-my-zsh/themes/agnoster_.zsh-theme $HOME/.oh-my-zsh/themes/agnoster_.zsh-theme'
  create_symlink('.zshrc', 'zsh/zshrc')
  create_symlink('.zshprofile', 'zsh/zshprofile')
end

task :configure_vim do
  system 'git clone https://github.com/gmarik/Vundle.vim.git ~/dotFiles/vim/bundle/Vundle.vim'
  create_symlink('.vim', 'vim')
  create_symlink('.vimrc', 'vim/vimrc')
  system 'vim +PluginInstall +qall'
end

task :configure_git do
  create_symlink('.gitconfig', 'git/gitconfig')
end

task :configure_tmux do
  create_symlink('.tmux.conf', 'tmux/tmux.conf')
end

task :configure_xmodmap do
  create_symlink('.xmodmap', 'xmodmap')
  system 'xmodmap $HOME/.xmodmap'
end

def create_symlink(path, dotfile)
  path, dotfile = homify(path), homify('dotFiles/' + dotfile)
  if File.exists?(path)
    p "#{path} already exists, do you want to replace it?"
    $stdin.gets.chomp == 'y' ? File.delete(path) : return
  end
  system "ln -s #{dotfile} #{path}"
end

def homify(path)
  Dir.home + '/' + path
end
