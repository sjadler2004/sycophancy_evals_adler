# sycophancy_evals_adler

This is a README for Steven Adler's project to test ChatGPT for sycophancy and to create/adapt simple, useful sycophancy evaluations.

This repo has a few components:

1. A Jupyter notebook, with code for converting an evaluation run to a visualization of sycophancy/contrarianism.
2. Results files from my having run evaluations
3. Datasets that feed into evaluations
4. A .yaml file, which has various evaluation configurations
5. A modified file from the Evals repo, which you'll need to replace in that repo to run tests on `chatgpt-4o-latest`

I apologize that the .yaml in particular is so messy. I ran a bunch of experiments in quick succession, and didn't want to refactor the names of the specific evaluations.

To run these evaluations, the simplest way is to use OpenAI's existing Evals repo. In particular, you only need to do 2 things:

1. Put the file `sycophancy` into `/evals/evals/registry/data`
2. Replace a file in Evals: ... into ` ` Make a change in Evals to be able to run `chatgpt-4o-latest` as a model - replace [$FILE] with [ 

