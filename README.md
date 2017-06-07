# FAITH Catholic web team documentation

## Setting up Mac for Drupal development + Ruby Sass

### Initial setup:

1. Install/Update Xcode from Mac app store. Open and accept license agreement.
2. Download and install Acquia devdesktop https://www.acquia.com/downloads
3. Install node.js https://nodejs.org/dist/v4.5.0/node-v4.5.0.pkg
4. Open terminal. Edit .bash_profile `vim .bash_profile`
5. OPTIONAL - Set nicer prompt - Add `export PS1="\w:"` - to top of bash profile
6. Add `source ~/.profile` to the bash profile
7. Install Homebrew `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
8. Install RVM  `curl -sSL https://get.rvm.io | bash -s stable --ruby`
9. Edit .bash_profile again. `vim .bash_profile` Add - `/Users/USERNAME/.rvm/gems/ruby-VERSION/bin` to $PATH (modify USERNAME and VERSION)
10. Install GNU Compiler Collection `brew install homebrew/versions/gcc49` (this takes a while to install)
11. Install Core Utilities `brew install coreutils`
12. Download Composer `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`
13. Install Composer `php composer-setup.php`
14. Move composer to global bin `mv composer.phar /usr/local/bin/composer`

### Site specific setup:
1. In terminal, cd into theme directory. RVM will check which version of ruby is required. Install different ruby version if necessary
2. If a different version of Ruby is required by gems, create or modify the .ruby_version file with the desired version, then repeat step 1
2. Run `rvm requirements –with-gcc=clang`
3. Install bundler `gem install bundler`
4. Install required gems `bundle install`
5. Run `compass watch`


### Other useful tools to install:
1. Install Bower `sudo npm install -g bower`
2. Install Grunt `sudo npm install -g grunt-cli`
3. Install Gulp `sudo npm install --global gulp-cli`
4. Install Vagrant https://releases.hashicorp.com/vagrant/1.9.1/vagrant_1.9.1.dmg


Git clean command alias gitclean='find . -name ".git" -exec rm -Rf {} \;'
