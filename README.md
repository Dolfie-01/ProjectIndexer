
# Project Indexer

## Overview

`Project Indexer` is a simple script designed to index the locations of classes, files, and other components within a project. This indexing allows **Large Language Models (LLMs)** to quickly understand the project's structure, enabling **D.R.Y. (Don't Repeat Yourself) coding** by preventing redundant object creation and avoiding full project scans.

By providing an organized index, `Project Indexer` enhances the LLM's understanding from the outset. When combined with a **well-structured design document** containing patterns and examples, it facilitates **efficient onboarding** for new tasks or ongoing development in an active codebase.

It works with C#, because thats what i use, so the Regex is set for this, but changing the Regex should enable you to Work with other programming files. 

## Why Use ProjectIndexer?

- **Reduces unnecessary LLM scanning**: Saves token usage compared to constant back-and-forth querying.
- **Prevents hallucinations**: Helps LLMs recognize what exists in the codebase.
- **Speeds up development**: Ideal for large projects with many files and classes.
- **Compatible with multiple LLMs**, including:
  - RooCode - the Awasome VSCode AI Developement Extension. 
  - Gemini (All)
  - Sonnet (All)
  - o3-mini and o3-mini-high
  - Deepseek V3.1 & Deepseek R1
  - GPT models
  - Grok

## Features

- **Creates** a **.json  file** listing class names, methods and locations.
- **Lightweight**: Only indexes names and locations, not full class properties or implementations.
- **Supports integration with RooCode**: In some cases, you can configure `Code/Architect` mode to frequently refer to `ProjectIndex.json`. You may also set it to **run **``** periodically** upon reaching milestones or creating new tasks.

> **Note:** This tool was built for personal use due to managing a **VS Solution with 5 projects and over 600 classes/methods**.

## Installation & Usage

Open the Project_Indexer.py File on line 54, change the Path to your Projects Root Location

 1. Drop `Project_Indexer.py` into the root of your project.

 2. Run the script via the command line - in the root of your Project. :

```sh
python Project_Indexer.py
```

 3. The script will generate `ProjectIndex.json`.

 4. Direct your LLM to read `ProjectIndex.json` for efficient project awareness.

I hope this is Usefull.

Happy coding! 

## Contributing

Feel free to fork the repository and submit pull requests for improvements!

## License

This project is licensed under the [MIT License](LICENSE).

---


