# CloudGPU notebooks

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mrhy7176/cloudgpu-notebooks/blob/main/chunked-cosine-cpu.ipynb)

`chunked-cosine-cpu.ipynb` is a CPU-only NumPy exercise that checks a chunked cosine-search implementation against an independent dense reference. It uses synthetic unit-normalized vectors, planted nearest neighbors, uneven chunks, and deliberate corruptions that the validator must reject.

This is a correctness exercise, not a GPU benchmark, a service endorsement, or a measurement of model quality. No account key, model download, external dataset, or network call is required. Use a CPU runtime with NumPy, and do not enable Python's optimization flag: the validator uses assertions.

Open the notebook in Colab with the badge above, or run the same file in JupyterLab. Related article (the article uses PyTorch; this notebook is a distinct CPU-only adaptation and does not test the article's CUDA path):

[Build and verify chunked cosine search with Python and PyTorch on a rented GPU](https://dev.to/cloudgpu_app/build-and-verify-chunked-cosine-search-with-python-and-pytorch-on-a-rented-gpu-5ep1)

[CloudGPU](https://cloudgpu.app/?utm_source=github&utm_medium=notebook&utm_campaign=20261111_exposure)

Disclosure: the maintainer works on CloudGPU. AI assisted the preparation of this notebook.

## License

MIT. See [LICENSE](LICENSE).
