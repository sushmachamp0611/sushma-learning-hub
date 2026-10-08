**Framework**: suppose one is asked to cut 5*5 mm paper one piece. its easy. But if one has to cut 1000 papers of 5*5 mm its tedious. there comes the solution that is get 5*5 frame
**Software framework** : common libraries + tools
LLM: trained once with x data (misses domain knowledge, latest news etc) 

Agentic AI frameworks: Langchain, Langgraph, Llamaindex 
**Langchain**: framework to build application by using multiple LLM for different tasks

**Huggingface** is open platform - AI models + datasets + space. 
simple analogy for hugging face : github is for code(receipe) like that Huggingface is for AI models(trained chefs)

**OpenAI** is an AI labortory and provided powerful LLM like GPT-3, ChatGPT, Codex, Whisper. 
GPT-3 Generative pretrained Tranformer - can generate human like texts, NLP question answering, summrize etc
ChatGPT is flagship product trained with billion parameters. Same as GPT plus user interface 
Codex: codex is even considered as an AI system developed by Openai, ​which has used publicly available code and train the model in ​such a way that it is capable of providing code snippets. ​And it can also suggest the best fitted code for your implementation.
DALL-E: Image generation that dont exist by providing text. 
OpenAi API: provides API to access all its models

Use Cases: Customer support and virtual assistant, Content creation an copywriting, Programming and Code Generation, Content Moderation. Personalized Recommendations

We need openAPI key to use above models


<img width="817" height="396" alt="image" src="https://github.com/user-attachments/assets/d26f3a8c-05d1-44dc-8f39-969a955342f3" />






**LangChain Modules**

<img width="917" height="467" alt="image" src="https://github.com/user-attachments/assets/292539a8-761b-4000-a85b-6bef77d58204" />









<img width="897" height="462" alt="image" src="https://github.com/user-attachments/assets/1140b2ca-cf63-4cb0-9ccd-5ea23c9dcd78" />









<img width="917" height="407" alt="image" src="https://github.com/user-attachments/assets/7120fbca-d1b9-49a4-9f04-98bcb433afb6" />




<img width="907" height="427" alt="image" src="https://github.com/user-attachments/assets/17967ead-cfcf-44a8-8d88-530c8e47259e" />





**Text Embedding** 


<img width="662" height="456" alt="image" src="https://github.com/user-attachments/assets/7e4b1076-d7bb-426f-84a6-558fb85fefa5" />











**Prompt Module Concept**
A PromptTemplate is a reusable structure for prompts.It lets you define a template string with placeholders and fill them dynamically.Purpose: ensures consistency, reduces repetition, and makes prompts modular.



<img width="736" height="422" alt="image" src="https://github.com/user-attachments/assets/e0542c92-724e-4b0a-b452-d6c03afa44f2" />









**Memory Module**
Conversational memory is what enables chatbots to retain conversation memory while having chat. Even though chatbot are stateless and have to implement conversational memory to give context aware responses 

| Memory Type | What It Stores | Best Use Case |
| --- | --- | --- |
| Buffer Memory | Full chat history | Short sessions |
| Buffer Window Memory | Last N turns | Lightweight context |
| Summary Memory | Summarized history | Long chats |
| Entity Memory | Facts about entities | Tracking people/things |
| Combined Memory | Mix of types | Balanced approach |
| Vector Store Memory | Semantic embeddings | Long-term recall |

LangChain offers multiple memory types — from simple buffers to semantic vector stores — so you can balance context length, efficiency, and relevance in conversational AI.
Code Snippet:
python
from langchain.memory import ConversationBufferMemory
memory = ConversationBufferMemory()
memory.save_context({"input":"Hi"}, {"output":"Hello!"})
print(memory.load_memory_variables({}))


**ChatGPT Clone**
Concept: Build a conversational app using ChatOpenAI with memory.
Key Idea: Multi-turn dialogue with context retention.

Code Snippet:
python
from langchain_openai import ChatOpenAI
from langchain.chains import ConversationChain

llm = ChatOpenAI(model="gpt-4o-mini", api_key="YOUR_API_KEY")
chain = ConversationChain(llm=llm, verbose=True)
print(chain.run("Hello, who are you?"))

**Prompt Engineering & Templates**
Concept: Structure prompts for consistency and reuse.
Types: PromptTemplate, ChatPromptTemplate, FewShotPromptTemplate.
Code Snippet:
python
from langchain.prompts import PromptTemplate
template = PromptTemplate.from_template("Tell me a joke about {animal}")
print(template.format(animal="cat"))

 **Chains**
Concept: Combine multiple steps (prompt → model → output).
Types: LLMChain, SequentialChain, ConversationChain.

Code Snippet:
python
from langchain.chains import LLMChain
from langchain.prompts import PromptTemplate
llm = OpenAI(model="gpt-4o-mini", api_key="YOUR_API_KEY")
prompt = PromptTemplate.from_template("Translate {text} to French")
chain = LLMChain(llm=llm, prompt=prompt)
print(chain.run("Hello world"))
6. Tools & Agents
Concept: Agents use tools (search, calculator, APIs) to answer queries.

Code Snippet:

python
from langchain.agents import load_tools, initialize_agent
tools = load_tools(["serpapi", "llm-math"], llm=llm)
agent = initialize_agent(tools, llm, agent="zero-shot-react-description", verbose=True)
print(agent.run("What's 2+2 and latest news on AI?"))

**Retrieval-Augmented Generation (RAG)**
Concept: Combine LLM with vector search for knowledge grounding.
Code Snippet:
python
from langchain.vectorstores import FAISS
from langchain.embeddings import OpenAIEmbeddings
docs = ["LangChain is powerful", "RAG improves accuracy"]
db = FAISS.from_texts(docs, OpenAIEmbeddings(api_key="YOUR_API_KEY"))
retriever = db.as_retriever()
print(retriever.get_relevant_documents("What is LangChain?"))

**LangGraph**
Concept: Graph-based orchestration of LLM workflows.
Key Idea: Define nodes (LLMs, tools) and edges (data flow).
Code Snippet (simplified):
python
from langgraph.graph import Graph
graph = Graph()
graph.add_node("llm", llm)
graph.add_edge("llm", "output")
result = graph.run("Hello!")
print(result)

