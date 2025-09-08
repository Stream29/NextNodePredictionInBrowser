# Transformer in Browser: Predict Next Node in Dify Workflow

This project is a interesting trial to run a Transformer model in the browser. I got a lot of fun of it.

## Preview

GitHub page: [https://stream29.github.io/NextNodePredictionInBrowser/index.html](https://stream29.github.io/NextNodePredictionInBrowser/index.html)

## Story: to Vibe a Transformer Model

While doing an internship at [Dify](https://dify.ai), I found it inconvenient to edit a workflow, 
which is far from the experience of AI completion in code editors.

Then I came up with this idea: Why not train a small model that can predict the next node in a workflow?
This is a simple task, so we only need a small model.
As the model is small enough, we can even run it in the browser.

Transformer is not a new technology, and we have a bunch of libraries to build/run a Transformer model.
So I made a bold decision: I would try to vibe a model.
I cloned the [Awesome-Dify-Workflow](https://github.com/svcvit/Awesome-Dify-Workflow) repository to my workspace.
Then I tell Claude Code to extract the node sequences from the Dify workflow DSL with a Python script.
It was done well undoubtedly. I easily extract a dataset from a set of workflows.
Then I told Claude Code to create a project with uv and train a Transformer model with the dataset.
It did work, but the model is stored in memory and pytorch specific.
So I told Claude Code to export the model to ONNX format and create a simple web page to run it in the browser.

All the steps above are done with telling Claude Code to write a report document in Markdown for context managing.
Thus, I trained a small Transformer model to predict the next node in a Dify workflow that can be run in the browser, 
without any coding. You can call it "vibe a model" just like "vibe coding".

## What I learned

- AI libraries are more mature than I thought.
- Training a model is not a so-great thing. It's trivial work that can even be done with pure vibe.
- If you have a good idea, you can train/fine tune a model to do it.
- If you already have enough knowledge on something, you can believe you can vibe it easily with updating stronger models.
- File system is a great repository for coding agent to store/fetch/update context, which makes context engineering much easier.
