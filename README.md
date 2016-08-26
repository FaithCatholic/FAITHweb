# FAITH Catholic web team documentation

## Setting up Mac for Drupal development

### Initial setup:

1. Install/Update Xcode from Mac app store. Open and accept license agreement.
2. Download and install Acquia devdesktop https://www.acquia.com/downloads
3. Install node.js https://nodejs.org/dist/v4.5.0/node-v4.5.0.pkg
4. Open terminal. Edit .bash_profile `vim .bash_profile`
5. OPTIONAL - Set nicer prompt - Add - `export PS1="\w:"` - to top of bash profile
6. Add - `source ~/.profile` to the bash profile
7. Install Homebrew `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
8. Install RVM  `curl -sSL https://get.rvm.io | bash -s stable --ruby`
9. Edit .bash_profile again. `vim .bash_profile` Add - `/Users/username/.rvm/gems/ruby-2.3.0/bin` to $PATH
10. Install gcc49 `brew install homebrew/versions/gcc49` (this takes a while to install)
11. Install Core Utilities `brew install coreutils`
12. Download Composer `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`
13. Install Composer `php composer-setup.php`
14. Move composer to global bin `mv composer.phar /usr/local/bin/composer`

### Site specific setup:
1. In terminal, cd into theme directory. RVM will check which version of ruby is required. Install different ruby version if necessary
2. Run `rvm requirements –with-gcc=clang`
3. Install bundler `gem install bundler`
4. Install required gems `bundle install`
5. Run `compass watch`

### OPTIONAL: If you would like to use grunt to run compass:
1. Install Grunt `sudo npm install -g grunt-cli`
2. Install packages `npm install`
3. To ensure livereload is enabled, look in Gruntfile.js Under sass: { - set livereload to `true`
4. Run `grunt watch`

