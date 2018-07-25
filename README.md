# install brew

##

# install python3

brew install python3

##

# add to .bashrc

export PATH="${HOME}/brew/bin:${HOME}/brew/sbin:/usr/local/bin:${PATH}:${HOME}/bin" # make sure brew bin dir is first in path

export WORKON_HOME=$HOME/.virtualenvs                 

export PIP_VIRTUALENV_BASE=$WORKON_HOME               

export PIP_RESPECT_VIRTUALENV=true                    

export VIRTUALENV_PYTHON=${HOME}/brew/bin/python3     

. ${HOME}/brew/bin/virtualenvwrapper.sh               

##

# install virtualenvwrapper

pip install virtualenv virtualenvwrapper

## 

mkdir -p ${HOME}/Projects/

cd ${HOME}/Projects

git clone https://github.com/danhimalplanet/inventory_control

cd ${HOME}/Projects/inventory_control  

mkvirtualenv inventory_control

pip install -r requirements.txt

workon inventory_control

heroku auth:login

heroku create

git push heroku master
