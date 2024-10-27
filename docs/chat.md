# PaperCraftr Chat Feature Tutorial 💬✨

![chat](https://res.cloudinary.com/dyknhuvxt/image/upload/v1729551304/chat-example_hdo9yu.png)

## Getting Help in Chat

At any time, if you're unsure of what commands are available or how to use them, you can get help within the chat by typing:

```bash
help()
```

This will provide a list of available commands and their usage.

## Using Multi-word Prompts

When interacting with the PaperCraftr assistant, it's important to enclose multi-word inputs in quotes to ensure they are processed as a single cohesive prompt. For example:

`[You]: "Explain the methodology used in the cognitive behavior analysis."`

This ensures that the assistant treats the entire input as one argument rather than splitting it into separate terms.

**Bonus!** The assistant is pre-loaded with the full PaperCraftr documentation, so you can ask it about any command or feature. For example, if you need help with a specific command:

`[You]: "Show me how to use the insert-section command and its parameters."`

This will provide you with clear guidance directly within the chat, ensuring you have everything you need to use PaperCraftr to its full potential!

## Overview

The **Chat** feature in **PaperCraftr** allows you to interact directly with the AI assistant to brainstorm ideas, refine content, or improve any aspect of your academic paper in real time. The feature includes the ability to prompt specific commands related to research refinement, structural adjustments, and citation management, all from within the chat environment. This guide will help you get started with using the chat feature effectively.

## Getting Started with Chat

Before you can use the chat feature, ensure that you have **PaperCraftr** installed and that your paper project is initialized. Once your project is ready, you can start a chat session with this command:

```bash
papercraftr chat --paper-path /path/to/your/paper
```

### Example:

```bash
papercraftr chat --paper-path ~/projects/cognitive-behavior-study
```

Once the session starts, you’ll be able to type messages to the assistant and receive responses directly in your terminal.

## Available Commands within Chat

While in a chat session, you can use commands to quickly execute tasks that PaperCraftr supports, such as refining your outline, improving sections, or updating your references. These commands provide flexibility, allowing you to iterate on various aspects of your paper without leaving the chat.

### Command Examples

You can trigger the following commands within the chat by typing the appropriate prompt.

### **Iterate**: Refining the Paper Iteratively

The **Iterate** commands are designed to help you iteratively improve the paper's content. You can refine specific aspects such as reference formatting, hypotheses, or the central argument.

- **Check references**:

  ```bash
  !iterate check-references "Ensure all references are formatted correctly."
  ```

- **Refine hypothesis**:

  ```bash
  !iterate refine-hypothesis "Refine the hypothesis in the context of cognitive behavior studies."
  ```

- **Check consistency**:

  ```bash
  !iterate check-consistency "Ensure consistency in research objectives and terminology."
  ```

- **Insert a section**:

  ```bash
  !iterate insert-section 2 "Insert a section discussing recent findings in AI's application in cognitive psychology."
  ```

### **Outline**: Structuring Your Paper

The **Outline** commands help you generate or refine various components of your paper's structure, including the abstract, main sections, or the conclusion.

- **General outline**:

  ```bash
  !outline general-outline "Summarize the overall structure of a research paper on AI in cognitive psychology."
  ```

- **Main points**:

  ```bash
  !outline main-points "Identify key points in the argument about AI's impact on cognitive processes."
  ```

- **Research summary**:

  ```bash
  !outline research-summary "Summarize recent research findings related to AI in behavioral studies."
  ```

### **Define**: Setting the Core Concepts and Research Questions

With **Define** commands, you can establish core components like your research question, hypothesis, and primary contributions of your study.

- **Define core research question**:

  ```bash
  !define research-question "Establish the main research question regarding AI's influence on cognitive processes."
  ```

- **Define primary contribution**:

  ```bash
  !define contribution "Define the primary contribution of this research in advancing AI applications in cognitive science."
  ```

### **References**: Managing and Formatting Citations

The **References** commands focus on handling citations and references throughout your paper. You can also add, format, and organize references with this command group.

- **Add a new reference**:

  ```bash
  !references add "Smith, J. (2022). Advances in AI for Cognitive Analysis."
  ```

- **Organize bibliography**:

  ```bash
  !references organize "Format and arrange all references in APA style."
  ```

## Exiting the Chat

When you're ready to exit the chat, simply type:

```bash
exit()
```

This will end the chat session and return you to the terminal.

## Conclusion

The **PaperCraftr Chat** feature, combined with powerful commands like **Iterate**, **Outline**, **Define**, and **References**, provides you with everything you need to write and refine your academic paper efficiently. Whether you are refining existing sections or managing your references, this feature allows you to enhance your research and writing process with ease.

---

Happy researching and refining with **PaperCraftr** and its powerful chat feature! ✍️✨
