# Welcome to *abstract2paper*: the solution to your writer's block!
Author: [Jeremy R. Manning](http://www.context-lab.com/)

## Step right up, step right up!
<img src='https://media1.giphy.com/media/mL40PfXA394KA/giphy.gif' width='250px'>

**Writing papers got you down?** Come on in, friend!  Give my good ole' Abstract2papers Cure-All a quick try!  Enter your abstract into the little [doohicky here](https://github.com/ContextLab/abstract2paper/blob/main/resources/abstract2paper_colaboratory.ipynb), and quicker'n you can blink your eyes<sup>1</sup>, a shiny new paper'll come right out for ya!  What are you waiting for?  Click the "doohicky" link above to get started, and then click the link to open the demo notebook in [Google Colaboratory](colab.research.google.com/).

To run the demo as a Jupyter notebook (e.g., locally), use [this version](https://github.com/ContextLab/abstract2paper/blob/main/resources/abstract2paper_jupyter.ipynb) instead.  Note: to compile a PDF of your auto-generated paper (when you run the demo locally), you'll need to have a working [LaTeX](https://www.latex-project.org/get/) installation on your machine (e.g., so that `pdflatex` is a recognized system command).  The notebook will also automatically install the [transformers](https://huggingface.co/transformers) library if it's not already available in your local environment.

In its unmodified state, the demo notebooks use the abstract from the [GPT-3 paper]() as the "seed" for a new paper.  Each time you run the notebook you'll get a new result, but an example PDF (generated using the smaller 1.3B parameter model) may be found [here](https://github.com/ContextLab/abstract2paper/blob/main/auto.pdf), and the associated .tex file may be found [here](https://github.com/ContextLab/abstract2paper/blob/main/auto.tex).

## How does it work, you ask?

Really it's quite simple.  We put in a smidgen of [this](https://huggingface.co/transformers/model_doc/gpt_neo.html) a pinch of [that](https://www.tug.org/texlive/), plus a dab of our special [*secret ingredient*](https://www.youtube.com/watch?v=dQw4w9WgXcQ), and **poof!** that's how the sausage is made.

## No really, how does it work?

Ok, if you really want to know, all I'm doing here is using the [Hugging Face](https://huggingface.co/) [implementation](https://huggingface.co/transformers/model_doc/gpt_neo.html) of [GPT-Neo](https://github.com/EleutherAI/gpt-neo), which is itself a tweaked version of [GPT-3](https://arxiv.org/abs/2005.14165) that is pre-trained on the [Pile](https://pile.eleuther.ai/) dataset.

The text you input is used as a prompt for GPT-Neo; to generate a document containing an additional *n* words, the model simply "predicts" the next *n* words that will come after the specified prompt.

With a little help from some basic [LaTeX](https://www.latex-project.org/) templates (borrowed from [Overleaf](https://www.overleaf.com)), the document is formatted and compiled into a PDF.

## Can I actually use this in real-world applications?

<img src='https://media4.giphy.com/media/3o6ozoD1ByqYv7ARIk/giphy.gif' width='250px'>

**Doubtful.**  Or at least, probably not...?  It certainly wouldn't be ethical to use this code to generate writing assignments, mass-produce papers or grant applications, etc.  Further, you'll likely find that the text produced using this approach includes stuff that's said in funny (often nonsensical) ways, follows problematic logic, incorporates biases from the training data, and so on.  Of lesser importance, but practical annoyance, you'll also encounter all sorts of formatting issues (although those might be easy to fix manually, and possibly even automatically with some clever tinkering).

# ⚠️ Disclaimers ⚠️

This demonstration is provided *as is*, and you choose to run it at your own risk.  The GPT-Neo model is trained on a large collection of documents from a variety of sources across the Internet.  Some of the text it's trained on includes potentially triggering and/or biased and/or horrible and/or disgusting-in-other-ways language.  That means that the text the model produces in the demo may also include disturbing language.  **If you don't want to risk exposure to that sort of text, then you should not run the notebook.**

Further, if you run the demo locally, it may mess up your compute environment, cause your stock portfolio to lose value, trigger the formation of a small-to-medium-sized black hole underneath your chair, put you in a bad mood, and/or otherwise mess up your day/week/month/year/life.  **Proceed with caution.**

&nbsp;
&nbsp;
&nbsp;
&nbsp;

<sup>1</sup><small>This claim rests on the assumption that you blink *really* slowly.  Depending on how much text you're trying to generate (and how long your prompt is), your paper could take anywhere from a few minutes to several hours to fully congeal.</small>
