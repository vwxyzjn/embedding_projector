## Setup

if you have poetry:
```bash
pyenv install -s $(sed "s/\/envs.*//" .python-version)
pyenv virtualenv $(sed "s/\/envs\// /" .python-version)
poetry install
```

else
```bash
pip install -r requirements.txt
```

## Reproduce

```bash
python test_wandb.py
tensorboard --logdir logs/imdb-example/
```

You will see the projector in tensorboard's http://localhost:6006/, but not in the wandb run https://wandb.ai/costa-huang/tensorflow-projector/runs/1218h3xy?workspace=user-costa-huang