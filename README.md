# Improving DetectGPT: Zero-Shot Machine-Generated Text Detection using Probability Curvature

## Official implementation of the experiments in the [DetectGPT paper](https://arxiv.org/abs/2301.11305v1).

An interactive demo of DetectGPT can be found [here](https://detectgpt.ericmitchell.ai).

# Our Contributions

## In order to improve computational limitations of DetectGPT - which are primarly due to the text pertubation and masking functions - we have modified these functions by immplementing batch processing to mask multiple texts at once. In addition, we added an efficient retry mechanism that only retries failed perturbations for texts where the inital fill was unsuccessful. This method reduces unnecessary computation, where the old code reprocceses texts that were already successfully filled if some or even one of the texts failed

## When running expiriments change the logic in the provided scripts. Replace "run.py" with our new "run2.py" immplementation

## Enviroment Setup Instructions

First, install the Python dependencies:

    python3 -m venv env
    source env/bin/activate
    pip install -r requirements.txt

Second, run any of the scripts (or just individual commands) in `paper_scripts/`.

If you'd like to run the WritingPrompts experiments, you'll need to download the WritingPrompts data from [here](https://www.kaggle.com/datasets/ratthachat/writing-prompts). Save the data into a directory `data/writingPrompts`.

**Note: Intermediate results are saved in `tmp_results/`. If your experiment completes successfully, the results will be moved into the `results/` directory.**



## Citing the paper and original code
If our work is useful for your own, you can cite us with the following BibTex entry:

    @misc{mitchell2023detectgpt,
        url = {https://arxiv.org/abs/2301.11305},
        author = {Mitchell, Eric and Lee, Yoonho and Khazatsky, Alexander and Manning, Christopher D. and Finn, Chelsea},
        title = {DetectGPT: Zero-Shot Machine-Generated Text Detection using Probability Curvature},
        publisher = {arXiv},
        year = {2023},
    }