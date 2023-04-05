# Flax Examples

## Core examples

The examples from this directory.

Each example is designed to be **self-contained and easily forkable**, while
reproducing relevant results in different areas of machine learning.

As discussed in [#231], we decided to go for a standard pattern for all examples
including the simplest ones (like MNIST). This makes every example a bit more
verbose, but once you know one example, you know the structure of all of them.
Having unit tests and integration tests is also very useful when you fork these
examples.

Some of the examples below have a link "🕹Interactive🕹" that lets you run them
directly in Colab.

Image classification

- [MNIST](https://github.com/google/flax/tree/main/examples/mnist/) -
  [🕹Interactive🕹](https://colab.research.google.com/github/google/flax/blob/main/examples/mnist/mnist.ipynb):
  Convolutional neural network for MNIST classification (featuring simple
  code).

- [ImageNet](https://github.com/google/flax/tree/main/examples/imagenet/) -
  [🕹Interactive🕹](https://colab.research.google.com/github/google/flax/blob/main/examples/imagenet/imagenet.ipynb):
  Resnet-50 on ImageNet with weight decay (featuring multi host SPMD, custom
  preprocessing, checkpointing, dynamic scaling, mixed precision).

Reinforcement learning

- [Proximal Policy Optimization](https://github.com/google/flax/tree/main/examples/ppo/):
  Learning to play Atari games (featuring single host SPMD, RL setup).

Natural language processing

-  [Sequence to sequence for number
   addition](https://github.com/google/flax/tree/main/examples/seq2seq/):
   (featuring simple code, LSTM state handling, on the fly data generation).
-  [Parts-of-speech
   tagging](https://github.com/google/flax/tree/main/examples/nlp_seq/): Simple
   transformer encoder model using the universal dependency dataset.
-  [Sentiment
   classification](https://github.com/google/flax/tree/main/examples/sst2/):
   with a LSTM model.
-  [Transformer encoder/decoder model trained on
   WMT](https://github.com/google/flax/tree/main/examples/wmt/):
   Translating English/German (featuring multihost SPMD, dynamic bucketing,
   attention cache, packed sequences, recipe for TPU training on GCP).
-  [Transformer encoder trained on one billion word
   benchmark](https://github.com/google/flax/tree/main/examples/lm1b/):
   for autoregressive language modeling, based on the WMT example above.

Generative models

-  [Variational
   auto-encoder](https://github.com/google/flax/tree/main/examples/vae/):
   Trained on binarized MNIST (featuring simple code, vmap).

Graph modeling

- [Graph Neural Networks](https://github.com/google/flax/tree/main/examples/ogbg_molpcba/):
  Molecular predictions on ogbg-molpcba from the Open Graph Benchmark.

[#231]: https://github.com/google/flax/issues/231

## Repositories Using Flax

The following code bases use Flax and provide training frameworks and a wealth
of examples, in many cases with pre-trained weights:

- [HuggingFace Transformers](https://github.com/huggingface/transformers) is a
  very popular library for building, training, and deploying state of the art
  machine learning models.
  These models can be applied on text, images, and audio. After organizing the
  [JAX/Flax community week](https://github.com/huggingface/transformers/blob/master/examples/research_projects/jax-projects/README.md),
  they have now over 5,000
  [Flax/JAX models](https://huggingface.co/models?library=jax&sort=downloads) in
  their repository.

- [Scenic](https://github.com/google-research/scenic) is a codebase/library
  for computer vision research and beyond. Scenic's main focus is around
  attention-based models. Scenic has been successfully used to develop
  classification, segmentation, and detection models for multiple modalities
  including images, video, audio, and multimodal combinations of them.

- [Big Vision](https://github.com/google-research/big_vision/) is a codebase
  designed for training large-scale vision models using Cloud TPU VMs or GPU
  machines. It is based on Jax/Flax libraries, and uses tf.data and TensorFlow
  Datasets for scalable and reproducible input pipelines. This is the original
  codebase of ViT, MLP-Mixer, LiT, UViM, and many more models.

- [T5X](https://github.com/google-research/t5x)  is a modular, composable,
  research-friendly framework for high-performance, configurable, self-service
  training, evaluation, and inference of sequence models (starting with
  language) at many scales.



## Community Examples

In addition to the curated list of official Flax examples, there is a growing
community of people using Flax to build new types of machine learning models. We
are happy to showcase any example built by the community here! If you want to
submit your own example, we suggest that you start by forking one of the
official Flax example, and start from there.

|             Link              |       Author        |             Task type             |                               Reference                               |
| ----------------------------- | ------------------- | --------------------------------- | --------------------------------------------------------------------- |
| [matthias-wright/flaxmodels]  | [@matthias-wright]  | Various                           | GPT-2, ResNet, StyleGAN-2, VGG, ...                                   |
| [DarshanDeshpande/jax-models] | [@DarshanDeshpande] | Various                           | Segformer, Swin Transformer, ... also some stand-alone layers         |
| [google/vision_transformer]   | [@andsteing]        | Image classification, image/text  | https://arxiv.org/abs/2010.11929, https://arxiv.org/abs/2105.01601, https://arxiv.org/abs/2111.07991, ... |
| [JAX-RL]                      | [@henry-prior]      | Reinforcement learning            | N/A                                                                   |
| [DCGAN] Colab                 | [@bkkaggle]         | Image Synthesis                   | https://arxiv.org/abs/1511.06434                                      |
| [BigBird Fine-tuning]         | [@vasudevgupta7]    | Question-Answering                | https://arxiv.org/abs/2007.14062                                      |
| [jax-resnet]                  | [@n2cholas]         | Various resnet implementations    | `torch.hub`                                                           |

[matthias-wright/flaxmodels]: https://github.com/matthias-wright/flaxmodels
[DarshanDeshpande/jax-models]: https://github.com/DarshanDeshpande/jax-models
[google/vision_transformer]: https://github.com/google-research/vision_transformer
[JAX-RL]: https://github.com/henry-prior/jax-rl
[DCGAN]: https://github.com/bkkaggle/jax-dcgan
[BigBird Fine-tuning]: https://github.com/huggingface/transformers/tree/master/examples/research_projects/jax-projects/big_bird
[jax-resnet]: https://github.com/n2cholas/jax-resnet
[@matthias-wright]: https://github.com/matthias-wright
[@DarshanDeshpande]: https://github.com/DarshanDeshpande
[@andsteing]: https://github.com/andsteing
[@henry-prior]: https://github.com/henry-prior
[@bkkaggle]: https://github.com/bkkaggle
[@vasudevgupta7]: https://github.com/vasudevgupta7
[@n2cholas]: https://github.com/n2cholas

## Anatomy of a Flax Example

Most of our examples in this directory follow a structure that we found to work
well with Flax projects, and we strive to make the examples easy to explore and
easy to fork. In particular (taken from [#231])

- README: contains links to paper, command line, [TensorBoard] metrics
- Focus: an example is about a single model/dataset
- Configs: we use `ml_collections.ConfigDict` stored under `configs/`
- Tests: executable `main.py` loads `train.py` which has `train_test.py`
- Data: is read from [TensorFlow Datasets]
- Standalone: every directory is self-conained
- Requirements: are pinned in `requirements.txt`
- Boilerplate: is reduced by using [`clu`]
- Interactive: the example can be explored with a [Colab]

[#231]: https://github.com/google/flax/issues/231
[TensorBoard]: https://tensorboard.dev/
[`clu`]: https://pypi.org/project/clu/
[Colab]: https://colab.research.google.com/
