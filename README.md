# sycophancy_evals_adler

This is a README for Steven Adler's project to test ChatGPT for sycophancy and to create/adapt simple, useful sycophancy evaluations.

There are a few components:

1. Results files with raw data from the evaluations I ran
2. Datasets that can be used for evaluations
3. The code to re-run various evaluations and create visualizations, in a Jupyter notebook
4. A .yaml configuration file, which defines the different evaluations to run

The first step is to: 
* 1A. Unzip the file `sycophancy`. If you just want to access the datasets or results files, you can stop there. These are respectively in folders with hopefully self-explanatory names - either `eval_results`, `anthropic_raw_data`, `downsampled_transformed_data` (a random sample of Anthropic's raw data, transformed into OpenAI-suitable format), or `new_data` (the datasets I created around random numbers, colors, and gibberish words).
* 1B. If you want to use this to actually run new evals, you need to follow instructions in OpenAI's [Evals](https://github.com/openai/evals/tree/main) repo to install that, then put the unzipped file into `/evals/evals/registry/data`

Continuing along this path of running the evaluations - you need to do two more things:
*  2. Put `sycophancy.yaml` into `/evals/evals/registry/evals`
*  3. Make `chatgpt-4o-latest` a runnable model in the Evals repo. Specifically, add `"chatgpt-4o-latest"` to `CHAT_MODEL_NAMES = { ... }` in `/evals/evals/registry.py`

Happy to help answer questions for anyone looking to run follow-on experiments; please message me on Twitter (https://twitter.com/sjgadler/) if you don't have another contact for me. 

I apologize that the .yaml and dataset names in particular are so messy. I ran a bunch of experiments in quick succession, and didn't want to pause to refactor the names of the specific evaluations.

For looking through an eval run (from a results file), you might find it helpful to use the Logviz tool: https://github.com/naimenz/logviz
