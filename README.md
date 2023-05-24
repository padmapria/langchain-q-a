# Langchain
<b> LangChain is a powerful framework designed for developing applications driven by language models. </b> 
  
  The primary goal of the project is to leverage the capabilities of the LangChain framework to build a state-of-the-art question-answering system that could effectively extract answers from a variety of documents. By utilizing LangChain's robust features and tools, the project aimed to develop a highly advanced and efficient document-based question-answering system

- Question answering in this context refers to question answering over your document data. 
- Question answering involves fetching multiple documents, and then asking a question of them. The LLM response will contain the answer to your question, based on the content of the documents.

The datasource for this q&a project may be a pdf document or url.

<b> Steps perfomed in the project: </b>    

<b> 1) Loading Documents:</b> 
  - Utilized the DirectoryLoader from LangChain to load documents from a directory.
  - Additionally, used the TextLoader to load documents from a specific URL.
  - This allowed for convenient access to the document data for further processing.

<b> 2) Splitting Documents:</b> 
  - To handle larger documents effectively, employed the CharacterTextSplitter from LangChain.
  - By using this tool, split the document contents into smaller, manageable chunks.
  - This step enabled more efficient processing and indexing of the document data.

<b> 3) Embedding and Indexing:</b> 
  - Leveraged the FAISS vector store from LangChain for embedding and indexing.
  - Used the "from_documents" function in FAISS to process the document chunks.
  - With the help of the HuggingFaceEmbeddings instance, generated embeddings for the document contents and Stored these embeddings by creating an index over them.
  - This step allowed for fast retrieval of relevant documents during the question-answering process.
  
<b> 4) Index Creation:</b> 
  -Created an index for the document data to enable smart retrieval of relevant documents.
  - This optimization step allowed the system to access the most suitable documents for a given question without processing all the documents.
  - Leveraging the indexing capabilities of FAISS, saved time and resources during the question-answering process.

<b> 5) Question-Answering System:</b> 
  - Utilized a pre-built question-answering chain integrated with LangChain.
  - This chain incorporated the HuggingFaceHub as the language model (LLM).
  - The system fetched multiple documents related to the query from the created index.
  - Based on the content of the fetched documents, the system determined the most appropriate response.
  - By leveraging the indexing and retrieval capabilities, the question-answering system provided accurate and relevant answers.

All the step are performed with FREE & open source tools mainly HuggingFace library with LangChain, without using OpenAPI APIs which are paid. 

<b> Things to improve </b> : Using OpenAPI paid API will increase the accuracy.
