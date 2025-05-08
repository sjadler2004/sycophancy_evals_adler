# sycophancy_evals_adler

This is a README for Steven Adler's project to test ChatGPT for sycophancy and to create/adapt simple, useful sycophancy evaluations.

This repo has a few components:

1. A Jupyter notebook, with code for converting an evaluation run to a visualization of sycophancy/contrarianism.
2. Results files from my having run evaluations
3. Datasets that feed into evaluations
4. A .yaml file, which has various evaluation configurations

I apologize that the .yaml in particular is so messy. I ran a bunch of experiments in quick succession, and didn't want to refactor the names of the specific evaluations.

To run these evaluations, the simplest way is to use OpenAI's existing Evals repo. In particular, you only need to do 3 things:

1. Put the file `sycophancy` into `/evals/evals/registry/data`
2. Put `sycophancy.yaml` into `/evals/evals/registry/evals`
3. Make `chatgpt-4o-latest` a runnable model in the Evals repo. Specifically, add `"chatgpt-4o-latest"` to `CHAT_MODEL_NAMES = { ... }` in `/evals/evals/registry.py`
