#Provides an orchestration to bootstrap a rails server with Vagrant
Ref: https://railsbox.io/

##Requirements
```brew install caskroom/cask/brew-cask
brew cask install virtualbox
brew cask install vagrant
brew install ansible```


Your project structure must be like:

```project/
  app
  bin
  ...
  railsbox/
    ansible/
    development/
      Vagrantfile
  Gemfile
  ...```

##How to start

```cd /path/to/rails/project/railsbox/development
vagrant up```

Once it's done, you'll be able to login into it using vagrant ssh command. Your application is stored in /myapp directory.

##VM
Virtual machine can be controlled by running the following commands:

```vagrant up                      # To start VM
vagrant provision               # To re-run ansible playbook
vagrant halt                    # To stop VM
vagrant destroy                 # To destroy VM completely```


##unicorn
You can start and stop unicorn by running standard upstart commands:

```sudo start myapp
sudo stop myapp
sudo restart myapp``