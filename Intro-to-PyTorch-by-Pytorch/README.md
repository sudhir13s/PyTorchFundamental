# Introduction to PyTorch — by PyTorch

My notes and code while working through the official **"Introduction to PyTorch — YouTube Series"** from the PyTorch team.

- 📺 **Playlist:** [Introduction to PyTorch (PyTorch channel)](https://www.youtube.com/watch?v=IC0_FRiX-sw&list=PL_lsbAsL_o2CTlGHgMxNrKhzP97BaG9ZN)
- 📖 **Docs:** [pytorch.org · Introduction to PyTorch — YouTube Series](https://docs.pytorch.org/tutorials/beginner/introyt/introyt_index.html)

> This is a personal learning workspace. Each notebook mirrors one lesson in the series, pre-filled with the lesson's section headings so I can follow along and take notes.

## Lessons

| #  | Notebook | Lesson | Tutorial |
|----|----------|--------|----------|
| 01 | [`01_introduction.ipynb`](notebooks/01_introduction.ipynb) | Introduction to PyTorch | [link](https://docs.pytorch.org/tutorials/beginner/introyt/introyt1_tutorial.html) |
| 02 | [`02_tensors.ipynb`](notebooks/02_tensors.ipynb) | Introduction to PyTorch Tensors | [link](https://docs.pytorch.org/tutorials/beginner/introyt/tensors_deeper_tutorial.html) |
| 03 | [`03_autograd.ipynb`](notebooks/03_autograd.ipynb) | The Fundamentals of Autograd | [link](https://docs.pytorch.org/tutorials/beginner/introyt/autogradyt_tutorial.html) |
| 04 | [`04_building_models.ipynb`](notebooks/04_building_models.ipynb) | Building Models with PyTorch | [link](https://docs.pytorch.org/tutorials/beginner/introyt/modelsyt_tutorial.html) |
| 05 | [`05_tensorboard_support.ipynb`](notebooks/05_tensorboard_support.ipynb) | PyTorch TensorBoard Support | [link](https://docs.pytorch.org/tutorials/beginner/introyt/tensorboardyt_tutorial.html) |
| 06 | [`06_training_models.ipynb`](notebooks/06_training_models.ipynb) | Training with PyTorch | [link](https://docs.pytorch.org/tutorials/beginner/introyt/trainingyt.html) |
| 07 | [`07_model_understanding_captum.ipynb`](notebooks/07_model_understanding_captum.ipynb) | Model Understanding with Captum | [link](https://docs.pytorch.org/tutorials/beginner/introyt/captumyt.html) |

## Project structure

```
Intro-to-PyTorch-by-Pytorch/
├── notebooks/      # one notebook per lesson (follow-along + notes)
├── data/           # datasets downloaded by the notebooks (git-ignored)
├── models/         # saved checkpoints / weights (git-ignored)
├── requirements.txt
└── README.md
```

## Setup

This project uses the **shared `ml-py312` uv environment** (Python 3.12) — the same one used across the PyTorch Fundamentals projects. Do **not** create a project-local `.venv`.

```bash
# activate the shared env
source ~/.uv/envs/ml-py312/bin/activate

# (one-time) install/refresh the lesson dependencies into it
uv pip install --python ~/.uv/envs/ml-py312/bin/python -r requirements.txt
```

The notebooks are already pinned to the **`Python (ml-py312)`** Jupyter kernel, so they bind to this environment automatically in Jupyter, VS Code, or PyCharm. The kernel was registered with:

```bash
python -m ipykernel install --user --name ml-py312 --display-name "Python (ml-py312)"
```

Run the notebooks with `jupyter lab` (or open them in your IDE and pick the `ml-py312` kernel). They auto-detect the best available device — CUDA / Apple MPS / CPU — so the same code runs on any machine.

## Notes

- `data/` and `models/` are working directories — their contents are git-ignored, but the folders are kept via `.gitkeep`.
- TensorBoard logs (lesson 05) write to `runs/` — launch with `tensorboard --logdir runs`.
