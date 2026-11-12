# CloudGPU developer tools and CPU notebooks

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cloudgpu-app/cloudgpu-notebooks/blob/main/chunked-cosine-cpu.ipynb)

## Compatible API request preflight

Download `index.html` and open it locally. It inspects a synthetic chat-request body and base URL without sending an API request, fetching a model catalog, loading external scripts, or saving inputs. The optional CloudGPU link leaves the page only when you choose it. Never paste a real key or private prompt.

It flags common mistakes such as repeated `/v1`, an endpoint path used as a base URL, malformed JSON, missing model/messages, credential-like fields and a string `stream` value. This is a limited structural checker, not a complete protocol validator, security scanner, availability check or proof of endpoint/model compatibility. It does not inspect headers, feature support or model quality. Local Node.js logic/DOM-stub tests passed; browser and accessibility acceptance are not yet complete.

## CPU chunked cosine notebook

`chunked-cosine-cpu.ipynb` is a CPU-only NumPy correctness exercise. It compares chunked cosine scores and document IDs with an independent dense reference using synthetic normalized vectors, planted neighbors and uneven chunks. Deliberate corruptions must be rejected.

Run in a CPU Colab/Jupyter runtime with NumPy. The notebook needs no account key, model download, external dataset or network call; opening Colab itself uses its website, and a fresh environment may need NumPy installed. Do not enable Python optimization: validation uses assertions. This is not a GPU benchmark, a measurement of model quality, or a test of the separate CUDA/PyTorch article path.

Related article: [Build and verify chunked cosine search with Python and PyTorch on a rented GPU](https://dev.to/cloudgpu_app/build-and-verify-chunked-cosine-search-with-python-and-pytorch-on-a-rented-gpu-5ep1).

## Disclosure

I work on CloudGPU. AI assisted preparation.

[CloudGPU](https://cloudgpu.app/?utm_source=github&utm_medium=referral&utm_campaign=202611_gtm_tools)

## License

MIT. See [LICENSE](LICENSE).
