arduino_relay_mfc_controller installation instructions
------------------------------------------------------

* Create a new virtual environment if necessary::

    virtualenv --system-site-packages ~/virtualenvs/arduino_relay_mfc_controller

* Activate a virtual environment::

    source ~/virtualenvs/arduino_relay_mfc_controller/bin/activate

* Install dependencies::

    pip install flask --upgrade
    pip install flask-sijax --upgrade

* Clone bitbucket mercurial repositories::

    mkdir ~/mercurial
    cd ~/mercurial
    hg clone https://bitbucket.org/peterpolidoro/python_libs/
    hg clone https://bitbucket.org/peterpolidoro/arduino_relay_mfc_controller/

* Install python packages::

    cd ~/mercurial/python_libs/arduino_device
    python cleanup.py
    python setup.py install
    cd ~/mercurial/arduino_relay_mfc_controller/host/python
    python cleanup.py
    python setup.py install
