# Human Feedback-Based Joke Generator

This project implements a **Human Feedback-Based Joke Generator** using **LangChain**, **LangGraph**, and **Groq's LLM**. It leverages a graph-based state management system to generate jokes, receive human feedback, and improve jokes based on feedback.

## Features

- **Joke Generation**: Automatically generate jokes based on a given topic.
- **Human Feedback**: Capture human feedback on whether the joke was funny.
- **Feedback-Based Improvement**: Rewrite jokes based on human and LLM feedback.
- **State Management**: Uses LangGraph to manage the workflow.
- **Structured Evaluation**: Uses Pydantic models to capture structured feedback.

## Tech Stack

- **Python**
- **LangChain**
- **LangGraph**
- **Groq LLM**
- **Pydantic** for structured feedback
- **Dotenv** for managing environment variables

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up your environment variables by creating a `.env` file in the root directory:

   ```plaintext
   GROQ_API_KEY=<your-groq-api-key>
   ```

## Usage

1. Run the Jupyter Notebook to initiate the joke generation process.

2. The notebook follows a multi-step process:

   - **Generate Joke**: The LLM generates a joke based on the provided topic.
   - **Get Human Feedback**: The user is asked whether the joke was funny or not.
   - **Rewrite Joke (if needed)**: If the joke wasn't funny, the LLM receives feedback and generates a better joke.
   - **Loop Until Laughter**: This process repeats until the human finds the joke funny.

3. The output will include:

   - **Generated Joke**
   - **Human Feedback**
   - **Improved Joke (if applicable)**

## Example Workflow

1. **Input Topic**: Provide a topic like `Cats`.
2. **Generate Joke**: The LLM generates a joke about Cats.
3. **Feedback**: The user is asked whether they laughed or not.
4. **Rewrite Joke**: If not funny, the LLM generates an improved joke.
5. **Repeat**: The process repeats until the joke is accepted.

## Environment Variables

Ensure you set the following environment variable in your `.env` file:

```plaintext
GROQ_API_KEY=<your-groq-api-key>
```

