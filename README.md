# Transformer in Browser: Predict Next Node in Dify Workflow

This project is a interesting trial to run a Transformer model in the browser. I got a lot of fun of it.

## Preview

GitHub page: [https://stream29.github.io/NextNodePredictionInBrowser/index.html](https://stream29.github.io/NextNodePredictionInBrowser/index.html)

## Story: to Vibe a Transformer Model

During an internship at [Dify](https://dify.ai), I found it inconvenient to edit a workflow, 
which is far from the experience of AI completion in code editors.

Then I came up with this idea: Why not train a small model that can predict the next node in a workflow?
This is a simple task, so we only need a small model.
As the model is small enough, we can even run it in the browser.

With the idea, I decided the process to vibe this model:

- Create a directory as workspace and add `docs` subdirectory.
- Clone the [Awesome-Dify-Workflow](https://github.com/svcvit/Awesome-Dify-Workflow) repository to my workspace.
- Init the Python project with `uv`.
- Extract the node sequences from the Dify workflow DSL with a Python script.
- Train a Transformer model with the dataset with PyTorch.
- Export the model to ONNX format and create a simple web page to run it in the browser with `ONNX.js`.

All the steps above are done with telling Claude Code to write a report document in Markdown for context managing.
Thus, I trained a small Transformer model to predict the next node in a Dify workflow that can be run in the browser, 
without any coding. You can call it "vibe a model" just like "vibe coding".

## What I learned

- AI libraries are more mature than I thought.
- Training a model is not a so-great thing. It's trivial work that can even be done with pure vibe.
- If you have a good idea, you can train/fine tune a model to do it.
- If you already have enough knowledge on something, you can believe you can vibe it easily with updating stronger models.
- File system is a great repository for coding agent to store/fetch/update context, which makes context engineering much easier.
