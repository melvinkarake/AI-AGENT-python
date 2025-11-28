AI Agent (Python)

This project is a simple AI assistant in the terminal, built in Python.
The agent uses LangChain and LangGraph to control an OpenAI chat model and can perform basic “reason + act” tasks using tools.

What the agent does

* Starts in the terminal and shows a welcome message.
* The user can type messages and the agent responds.
* The chat continues in a loop until the user types `"quit"`.
* The agent has simple tools, such as:

  * a calculator tool to add two numbers
  * a `say_hello` tool to greet a user

How it roughly works (in plain language)

* A `.env` file contains the secret OpenAI API key.
* With `dotenv`, that API key is made available to the Python code.
* LangChain and LangGraph build an “agent” around the OpenAI model that:

  * reads the user’s message,
  * can decide whether a tool should be used,
  * calls the tool (e.g. calculator or `say_hello`),
  * and then sends a response back to the user.
* In `main.py` there is a while loop that:

  * reads the user’s input,
  * forwards the message to the agent,
  * shows the agent’s reply in the terminal,
  * stops as soon as the user types `"quit"`.

Requirements

* Python and a working development environment.
* A `.env` file with a valid OpenAI API key.
* A terminal (for example `uv` terminal or a regular command prompt) to run the script.

Limitation
At the moment I don’t have any credit on my OpenAI account.
This means the agent in the terminal cannot return real responses
as long as there is no credit linked to the API key being used.
If there is insufficient quota, the OpenAI API will return an error
and the agent’s response will stop.
