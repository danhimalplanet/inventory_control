# SETUP

mkdir -p ${HOME}/Projects/inventory_control

export WORKON_HOME=$HOME/.virtualenvs                 # put
export PIP_VIRTUALENV_BASE=$WORKON_HOME               # in
export PIP_RESPECT_VIRTUALENV=true                    # your
export VIRTUALENV_PYTHON=${HOME}/brew/bin/python3     # 
. ${HOME}/brew/bin/virtualenvwrapper.sh               # .bashrc

cd ${HOME}/Projects/inventory_control  
mkvirtualenv inventory_tracker

##

cd ${HOME}/Projects/inventory_control
workon inventory_control

heroku auth:login

