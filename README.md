# Be a windbag!

<img src="img/windbag.png" align="right"
     alt="Windbag logo" width="150" height="150">

Windbag is a simple RAG application that combines a local code base and Code Llama. 

You can read a detailed write up of this code [on my blog](https://www.thediscoblog.com/extending-code-llama/). 

Note that as coded, this application makes a large assumption that the indexed code is written in Ruby. It's easy enough to make this more generic, however. 

Set up is easy! Just run

```bash
% pip install langchain langchain-community
```

## Parameters

There are some parameters that can be passed to the code:

* The temperature. It can be set in the constructor of `ChatCode`.
* The model. It can also be set in the constructor of `Chatcode`.
* The language and the file suffixes. Both can be set as parameters to the
  `ingest()` method.

To use a model, you have to download it first, using Ollama or similar tools.

The suffixes are given as a list because a language may use several suffixes.
For example, C++ may use `.h`, `.cpp` and `.cxx`.
