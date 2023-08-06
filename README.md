## llama2.py

<p align="center">
  <img src="assets/llama_cute.jpg" width="300" height="300" alt="Cute Llama">
</p>

## Why this fork?

I think it's worthwhile to have a fork that implements Python version of `llama2.c` as a kind of simplest "reference implementation" for further educational purpose for wide audience.

Currently `llam2.c` contains 2`.py` files for training models and and 1 `.c` file for inference. There is a gap to have a simple reference implementation of all transformers logic in a simple Python file under 500 lines. While original FB/llama code also implemented in Python, I couldn't say that implementation is simple due to multiple dependencies and optimizations impelemnted.

PS. Performance is awful at the moment `~1 tok./sec`, there is a huge room for improvements. PRs are welcome 😄


## feel the magic

First, navigate to the folder when you keep your projects and clone this repository to this folder:

```bash
git clone https://github.com/tairov/llama2.py.git
```

Then, open the repository folder:

```bash
cd llama2.py
```

Now, let's just run a baby Llama 2 model in C. You need a model checkpoint. Download this 15M parameter model I trained on the [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories) dataset (~60MB download):

```bash
wget https://huggingface.co/karpathy/tinyllamas/resolve/main/stories15M.bin
```

Compile and run the C code:

```bash
python3 llama2.py stories15M.bin
```

## performance

Performance is awful at the moment. 
On my Mac M1 Max -- `~1.3 tok / sec`

## License

MIT
