# Prerequisites

- An Azure OpenAI deployment with both an embedding model and a chat model.
- Python installed on your machine. You can download it from [python.org](https://www.python.org/downloads/).

# Documentation

https://learn.microsoft.com/en-us/azure/ai-services/openai/

https://learn.microsoft.com/en-us/semantic-kernel/overview/


# Install semantic-kernel

`pip install semantic-kernel`

# Create a .env File

```
AZURE_OPENAI_CHAT_DEPLOYMENT_NAME="gpt-4o"
AZURE_OPENAI_ENDPOINT="https://ai-tesing-sk.openai.azure.com/"
AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME="text-embedding-ada-002"
AZURE_OPENAI_API_KEY="<your->"
```

# Run the samples

`python agants_chat.py`

`python agants_with_plugins.py`

`python function_calling_filtering.py`

`python function_calling`

`python rag.py`

# Write your own Copilot !

1. Check out the `function_calling.py` as a template to have a console interface.
2. Copy the content into a new File called `my_own_copiliot.py`
3. Create your own Plugin in the Plugins Folder
4. Import you plugin into the copiliot file `from plugins.<your-file> import <your-class-name>`
5. Add your own Plugin to the kernel `kernel.add_plugin(<YOUR PLUGIN CLASS>(), plugin_name="<YOUR PLUGIN NAME>")`
6. Try out your own copilot `python my_own_copiliot.py`