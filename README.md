# LLM-of-Full-Stack-Programmer-Supervisor

Full Stack Programmer Supervisor LLM used to help users with less experience or skills in the programming and IT fields. There are several main systems:

1. practice question generator
2. concept guidance system
3. code generator and guidance system
4. code evaluation system
5. general knowledge system

Gemini-2.0-flash model is used for all of my LLM response systems due to high performance in different cases(i.e. real-time streaming, multimodal understanding, etc) with less time consumption.


## Few-shot prompts¶

Few-shot prompts are used to guide LLM to handle and respond to users' queries in detail with several samples of queries and responses as references. It found in below several systems:

1. practice question generator
2. concept guidance system
3. code generator and guidance system
4. code evaluation system


## Context Window

Set 1000 as a maximum for practice question generator and concept guidance system, and 5000 tokens for code generator and guidance system. The main reason is to show a longer context window and a detailed explanation.


## Models in special

### concept guidance system

Verbal explanation is provided, including graph, table, flowchart.

### code generator and guidance system

To display the code in the output with a user-friendly UI, the programming language type is extracted from a markdown code block indicator.

### code evaluation system

The LLM model used to evaluate the code fetched from the URL with the f-string-typed query, so it is essential to convert the data type to fit the requirement.

### Model for general knowledge system¶

Grounding is used to connects the LLM to reliable external sources, dramatically reducing hallucinations and ensuring responses contain up-to-date, verified information. It can mitigate “AI Hallucination” from Google Search. I set the response be simple and brief with less than 100 words to save tokens.


## Function Calling

To use a suitable LLM according to the content of the user's query, function calling is used to respond with a single name from the different systems.


## Create a simple interactive chat¶

Type 'exit', 'q' or 'quit' to end the conversation.
