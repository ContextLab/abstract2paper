# Welcome to *abstract2paper*!
Author: [Jeremy R. Manning](http://www.context-lab.com/)

## Step right up, step right up!
<img src='https://media1.giphy.com/media/mL40PfXA394KA/giphy.gif' width='250px'>

**Writing papers got you down?** Come on in, friend!  Give good the Ole' Abstract2papers Cure-All a quick try!  Enter your abstract into the little [doohicky here](), and quicker'n you can blink your eyes<sup>1</sup>, a shiny new paper'll come right out for ya!  What are you waiting for?  (Click the "doohicky" link in the preceding sentence to get started.)

## How does it work, you ask?

Really it's quite simple.  We put in a smidgen of [this](https://huggingface.co/transformers/model_doc/gpt_neo.html) a pinch of [that](https://www.tug.org/texlive/), plus a dab of our special [*secret ingredient*](https://www.youtube.com/watch?v=dQw4w9WgXcQ), and **poof!** that's how the sausage is made.

## No really, how does it work?

Ok, if you really want to know, all I'm doing here is using the [Hugging Face](https://huggingface.co/) [implementation](https://huggingface.co/transformers/model_doc/gpt_neo.html) of [GPT-Neo](https://github.com/EleutherAI/gpt-neo), which is itself a tweaked version of [GPT-3](https://arxiv.org/abs/2005.14165) that is pre-trained on the [Pile](https://pile.eleuther.ai/) dataset.

The text you input is used as a prompt for GPT-Neo; to generate a document containing an additional *n* words, the model simply "predicts" the next *n* words that will come after the specified prompt.

With a little help from some basic [LaTeX](https://www.latex-project.org/) templates (borrowed from [Overleaf](https://www.overleaf.com)), the document is formatted and compiled into a PDF.

## Can I actually use this in real-world applications?

<img src='https://media4.giphy.com/media/3o6ozoD1ByqYv7ARIk/giphy.gif' width='250px'>

**Doubtful.**  Or at least, probably not...?  It certainly wouldn't be ethical to use this code to generate writing assignments, mass-produce papers or grant applications, etc.  Further, you'll likely find that the text produced using this approach includes stuff that's said in funny (often nonsensical) ways, follows problematic logic, incorporates biases from the training data, and so on.  Of lesser importance, but practical annoyance, you'll also encounter all sorts of formatting issues (although those might be easy to fix manually, and possibly even automatically with some clever tinkering).

&nbsp;
&nbsp;
&nbsp;
&nbsp;

<sup>1</sup><small>This claim rests on the assumption that you blink *really* slowly.  Depending on how much text you're trying to generate (and how long your prompt is), your paper could take anywhere from a few minutes to several hours to fully congeal.</small>
