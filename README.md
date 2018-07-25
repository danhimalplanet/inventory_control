mkdir -p ${HOME}/Projects/inventory_control

export WORKON_HOME=$HOME/.virtualenvs
export PIP_VIRTUALENV_BASE=$WORKON_HOME
export PIP_RESPECT_VIRTUALENV=true
export VIRTUALENV_PYTHON=${HOME}/brew/bin/python3

. ${HOME}/brew/bin/virtualenvwrapper.sh

cd ${HOME}/Projects/inventory_control

mkvirtualenv inventory_tracker

# 

mkdir -p ${HOME}/Projects/inventory_control
workon inventory_control
