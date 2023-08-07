## llama2.py


## Why this fork?

I think it's worthwhile to have a fork that implements Python version of `llama2.c` as a kind of simplest "reference implementation" for further educational purpose for wide audience.

Currently `llam2.c` contains 2`.py` files for training models and 1 `.c` file for inference. There is a gap to have a simple reference implementation of all transformers logic in a simple Python file under 500 lines. While original FB/llama code also implemented in Python, I couldn't say that implementation is simple due to multiple dependencies and optimizations impelemnted.

PS. Performance is awful at the moment `~1 tok./sec`, there is a huge room for improvements


## feel the magic

First, navigate to the folder when you keep your projects and clone this repository to this folder:

```bash
git clone https://github.com/tairov/llama2.py.git
```

Then, open the repository folder:

```bash
cd llama2.py
```

Now, let's just run a baby Llama 2 model in Python

```bash
wget https://huggingface.co/karpathy/tinyllamas/resolve/main/stories15M.bin
```

Just run the Python

```bash
python3 llama2.py stories15M.bin 0.8 256 "Dream comes true this day"
<s>
Dream comes true this day. To their surprise. A big game was easy and everyone was going on the day. Jack and they were playing beneath: life, free, butter! There was the time to think of the universe. There was very happy, fun and the joy and the following down below of this day they were there was a lot of a wide, new camping.
Jack and they had happened. The town was the saving up above the camp of the waves shor of their laughter, friendly journey of friendship to one. The night sky show of the end. Little ceremony, happy again.
<s>
 Once upon his family of a big day when Jack. They were filled foreshadowed happy and they were the joy filled this, different: the King of their appreciation they were to a wave to the spring limit. They were becoming Ruby, happy and the sunset of life of an amazing friendship and he had a robot.
<s>
 Once upon a 4, happy to the wonderful experience of the celebration of their friendship. Even the playground.
Jack and Sammy fishing adventure foreshium of a wishing being free time, happy. The generous adventure foreshly made it. The chance to
achieved tok/s: 1.3463711338028914
```

## performance

Performance is awful at the moment. 
On my Mac M1 Max -- `~1.3 tok / sec`

## License

MIT
