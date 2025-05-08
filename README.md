# sycophancy_evals_adler

This is a README for Steven Adler's project to test ChatGPT for sycophancy and to create/adapt simple, useful sycophancy evaluations.

This repo has a few components:

1. A Jupyter notebook, with code for converting an evaluation run to a visualization of sycophancy/contrarianism.
2. Results files from my having run evaluations
3. Datasets that feed into evaluations
4. A .yaml file, which has various evaluation configurations

To run these evaluations, the simplest way is to use OpenAI's existing Evals repo (https://github.com/openai/evals). In particular, you only need to do 3 things:

1. Put the file `sycophancy` into `/evals/evals/registry/data`
2. Put `sycophancy.yaml` into `/evals/evals/registry/evals`
3. Make `chatgpt-4o-latest` a runnable model in the Evals repo. Specifically, add `"chatgpt-4o-latest"` to `CHAT_MODEL_NAMES = { ... }` in `/evals/evals/registry.py`

Happy to help answer questions for anyone looking to run follow-on experiments; please message me on Twitter (https://twitter.com/sjgadler/) if you don't have another contact for me. 

I apologize that the .yaml and dataset names in particular are so messy. I ran a bunch of experiments in quick succession, and didn't want to pause to refactor the names of the specific evaluations.

For visualizing an eval run, you might find it helpful to use the Logviz tool: https://github.com/naimenz/logviz
