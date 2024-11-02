
# Setup

cd ~/work/canva
tools/build/bazel/bazel-run.sh //tools/build/python/third_party:setup_python_venv
export PYTHONPATH=$(pwd):$PYTHONPATH
source tools/build/python/third_party/.venv/bin/activate
pip install diffusers["torch"] transformers

# Notebook server

cd ~/work/canva
export PYTHONPATH=$(pwd):$PYTHONPATH
source tools/build/python/third_party/.venv/bin/activate

huggingface-cli login

jupyter lab --ip=0.0.0.0 --port=8888 --allow-root --notebook-dir ~/work/diffusers-hello-world

