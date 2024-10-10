# GPT from scratch

This repository contains implementations of Andrej Karpathy's Playlist on building GPT from scratch for practice purposes. GPT architecture from micrograd to the final GPT (and even GPT-2), using only basic pytohn and later with some pytorch as well. 

## Table of content
1) Micrograd
2) Makemore
    - Bigram
    - MLP, following Bengio et al. 2003
    - CNN, following DeepMind WaveNet 2016 (in progress...)
    - RNN, following Mikolov et al. 2010
    - LSTM, following Graves et al. 2014
    - GRU, following Kyunghyun Cho et al. 2014
    - Transformer, following Vaswani et al. 2017
3) NanoGPT
4) MiniBPE

I also plan on making a LLM in C but that is on hold. LLMs in simple, pure C/CUDA with no need for 245MB of PyTorch or 107MB of cPython. Current focus is on pretraining, in particular reproducing the [GPT-2](https://github.com/openai/gpt-2) and [GPT-3](https://arxiv.org/abs/2005.14165) miniseries, along with a parallel PyTorch reference implementation in [train_gpt2.py](train_gpt2.py). You'll recognize this file as a slightly tweaked [nanoGPT](https://github.com/karpathy/nanoGPT), an earlier project of mine. Currently, llm.c is a bit faster than PyTorch Nightly (by about 7%). In addition to the bleeding edge mainline code in [train_gpt2.cu](train_gpt2.cu), we have a simple reference CPU fp32 implementation in ~1,000 lines of clean code in one file [train_gpt2.c](train_gpt2.c). I'd like this repo to only maintain C and CUDA code. Ports to other languages or repos are very welcome, but should be done in separate repos, and I am happy to link to them below in the "notable forks" section. Developer coordination happens in the [Discussions](https://github.com/karpathy/llm.c/discussions) and on Discord, either the `#llmc` channel on the [Zero to Hero](https://discord.gg/3zy8kqD9Cp) channel, or on `#llmdotc` on CUDA MODE Discord.