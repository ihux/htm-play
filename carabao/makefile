# makefile to manage carabao toolbox

all:
	@echo '  make venv      # make virtual environment'
	@echo '  make install   # install packages for playground'
	@echo '  make carabao   # build carabao wheel and install'
	@echo '  make clean     # cleanup folder'
	@echo '  make scrap     # cleanup folder and scrap virtual environment'
	@echo ''
	@echo '  to activate virtual environment invoke: $ source venv/bin/activate'

venv:
	python3 -m venv venv
	deactivate 2>/dev/null
	@echo 'invoke: $ source venv/bin/activate'

install:
	deactivate 2>/dev/null
	#source venv/bin/activate
	pip install --upgrade wheel
	pip install  --upgrade setuptools
	pip install  --upgrade twine
	pip install pytest==4.4.1
	pip install pytest-runner==4.4
	python3 -m pip install --upgrade build
	pip install --upgrade numpy
	pip install --upgrade torch
	pip install jupyterlab

clean:
	rm -rf dist/

scrap:
	make clean
	rm -rf venv/
