# Langchain
LangChain is a powerful framework designed for developing applications driven by language models. 

This project aimed to build a state-of-the-art document based question-answering system using LangChain framework. 

- Question answering in this context refers to question answering over your document data. 
- Question answering involves fetching multiple documents, and then asking a question of them. The LLM response will contain the answer to your question, based on the content of the documents.

The datasource for the q&a may be a pdf document or url.

Steps perfomed in the project:
1) Loading Documents:

- Utilized the DirectoryLoader from LangChain to load documents from a directory.
- Additionally, used the TextLoader to load documents from a specific URL.
- This allowed for convenient access to the document data for further processing.

2) Splitting Documents:

- To handle larger documents effectively, employed the CharacterTextSplitter from LangChain.
- By using this tool, split the document contents into smaller, manageable chunks.
- This step enabled more efficient processing and indexing of the document data.

3) Embedding and Indexing:

- Leveraged the FAISS vector store from LangChain for embedding and indexing.
- Used the "from_documents" function in FAISS to process the document chunks.
- With the help of the HuggingFaceEmbeddings instance, generated embeddings for the document contents and Stored these embeddings by creating an index over them.
- This step allowed for fast retrieval of relevant documents during the question-answering process.
Index Creation:

4) Created an index for the document data to enable smart retrieval of relevant documents.
- This optimization step allowed the system to access the most suitable documents for a given question without processing all the documents.
- Leveraging the indexing capabilities of FAISS, saved time and resources during the question-answering process.

5) Question-Answering System:

- Utilized a pre-built question-answering chain integrated with LangChain.
- This chain incorporated the HuggingFaceHub as the language model (LLM).
- The system fetched multiple documents related to the query from the created index.
- Based on the content of the fetched documents, the system determined the most appropriate response.
- By leveraging the indexing and retrieval capabilities, the question-answering system provided accurate and relevant answers.


All the step are performed with FREE & open source tools mainly HuggingFace library with LangChain, without using OpenAPI APIs which are paid. 

Things to improve: Using OpenAPI paid API will increase the accuracy.