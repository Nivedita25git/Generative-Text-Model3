

---
GPT-2 Text Generation Web App

This project is a simple and interactive web-based application that demonstrates the text generation capabilities of **OpenAI's GPT-2 model** using **TensorFlow** and **Hugging Face Transformers**. The interface is created using **Gradio**, allowing users to input a prompt and receive coherent AI-generated text in response.

---

 Features

*  Based on OpenAI's **GPT-2** language model
*  Generate coherent and context-aware text completions
*  Interactive web UI using **Gradio**
*  Beam search decoding for improved output quality
* ⚙ Customizable prompt input

---

## Dependencies

Install required packages using pip:

```bash
pip install -q gradio
pip install -q git+https://github.com/huggingface/transformers.git
```

---

##  How It Works

1. The **GPT-2 tokenizer** encodes the user's prompt into token IDs.
2. The **TFGPT2LMHeadModel** (TensorFlow version of GPT-2) generates a response using **beam search decoding** to improve quality.
3. The generated token IDs are decoded back into natural language text.
4. The output is displayed through a Gradio web interface.

---

##  Sample Outputs

**Prompt 1:**
`The future of artificial intelligence is`
**Output:**

> The future of artificial intelligence is in the hands of the next generation of scientists and engineers.

**Prompt 2:**
`Once upon a time in a distant galaxy,`
**Output:**

> Once upon a time in a distant galaxy, a group of intelligent beings, known as the Guardians of the Galaxy...

---

##  Running the App

Simply run the Python script or Colab notebook:

```python
gr.Interface(
    fn=generate_text,
    inputs=gr.Textbox(label="Enter a prompt"),
    outputs=gr.Textbox(label="Generated text"),
    title="GPT-2",
    description="OpenAI's GPT-2 can generate coherent text. Input a sentence to see how it completes it."
).launch()
```

A local web server will be hosted (or a public URL will be provided in Colab) to interact with the model.

---

## Project Structure

```
├── app.py (or .ipynb)
├── README.md
```

---



---

