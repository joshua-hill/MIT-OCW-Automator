# MIT-OCW-Automator
Hackathon submission

# Free Degree Automator

This repository contains a Python notebook designed to automate the process of responding to assignments from MIT OpenCourseWare (OCW). It leverages OpenAI's GPT-4 for advanced natural language processing to parse, interpret, and solve assignment problems, including referencing relevant textbook material. It makes use of various custom classes, such as an ObjectiveReasoner class in order to provide the model an interna monologue and the ability to plan and gauge its completion of an objective.

## Features

- **Assignment Interaction**: Parses assignment prompts to extract course codes, assignment numbers, and problem statements.
- **Textbook Reference Extraction**: Utilizes a custom `ObjectiveReasoner` to interact with GPT-4, extracting targeted textbook references and page numbers.
- **PDF Generation**: Compiles solutions and generates a formatted PDF ready for submission.
- **Dropbox Integration**: (Future Feature) Automates the upload of the completed assignment PDF to Dropbox.

## To use the notebook:

Open the Free_Degree_Automator.ipynb in Jupyter Notebook or JupyterLab.
Follow the instructions within the notebook, entering your OpenAI API key where necessary.
Run the cells sequentially to perform the operations described in the comments.

## How It Works
The notebook is structured to follow the workflow of receiving an assignment to submitting a completed response:

Assignment Retrieval: It starts by downloading the assignment using playwright.
Problem Extraction: Parses the assignment PDF to identify problems using PyPDF2.
Solving Problems: Interacts with GPT-4 using the ObjectiveReasoner to solve each problem and reference textbooks when necessary.
Compiling Solutions: Solutions are compiled and checked for completion.
PDF Creation: Solutions are formatted and exported to a PDF document using reportlab.
