# rag-1

https://python.langchain.com/docs/tutorials/rag/


for message, metadata in graph.stream( 

    {"question": "What is Task Decomposition?"}, stream_mode="messages" 

): 

    # Estrai il testo 

    if isinstance(message.content, list): 

        text = "".join( 

            part["text"] for part in message.content if part["type"] == "text" 

        ) 

    else: 

        text = str(message.content) 

  

    # Split in parole e aggiungi il separatore | 

    words = text.split() 

    print("|" + "|".join(words), end="") 
