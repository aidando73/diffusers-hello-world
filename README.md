

cd ~/work/canva
export PYTHONPATH=$(pwd):$PYTHONPATH
source tools/build/python/third_party/.venv/bin/activate

huggingface-cli login

jupyter lab --ip=0.0.0.0 --port=8888 --allow-root --notebook-dir ~/work/hello-world
