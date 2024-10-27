# Getting Started with PaperCraftr 📑✨

**PaperCraftr** is part of the **AICraftr** suite and is designed to assist you in crafting academic papers with the help of AI. Inspired by structured research methodologies, this guide will walk you through creating a paper from scratch. Whether you're outlining, conducting literature reviews, or drafting sections, PaperCraftr provides support every step of the way.

Structured research emphasizes clarity in **contribution**, **framework**, and **writing process**, which we will follow throughout this guide.

## Step 1: Install AICraftr

To use PaperCraftr, first install the **AICraftr** suite, which includes StoryCraftr, using [pipx](https://pypa.github.io/pipx/), a tool to help you install and run Python applications in isolated environments. It works on most platforms, including macOS, Linux, and Windows. Using `pipx` ensures that **AICraftr** runs in its own virtual environment, keeping your system's Python installation clean.

To install **AICraftr**, run the following command:

```
pipx install git+https://github.com/raestrada/storycraftr.git@v0.7.3-alpha3
```

### Important: Before running the `papercraftr` command

Store the key in a text file located at `~/.papercraftr/openai_api_key.txt` for convenience.

```
mkdir -p ~/.papercraftr/
echo "your-openai-api-key" > ~/.papercraftr/openai_api_key.txt
```

Once installed and the API key is set, you can run the tool using the command `papercraftr`.

## Step 2: Create the Behavior File

The **behavior file** is essential to guide the AI’s **writing approach**. It represents the **researcher's perspective** and defines how the AI should approach the paper. This file goes beyond technical details—it sets the tone, style, and focus of the paper, establishing a foundation for the AI to align with your research goals.

The behavior file acts as a **creative guide** for the AI, helping ensure that all generated content follows your desired **tone**, **methodology**, and **academic style**.

### What Should Go in the Behavior File?

In the behavior file, you can include various elements to help guide the AI:

- **Research Focus**: What’s the central question or hypothesis?
- **Tone**: Should the writing be formal, technical, concise, etc.?
- **Methodology**: What approach should the AI follow in presenting data?
- **Literature Depth**: Does the paper require an extensive review, or is it focused on a narrow contribution?
- **Length**: Are you aiming for a conference paper, journal article, or thesis?
- **Structure**: Does your paper follow a standard format (like IMRaD) or a customized structure?

Here's an example:

```
echo "Write in a formal, structured tone focusing on a hypothesis-driven research paper. The paper should explore connections between AI and cognitive psychology, using a systematic review and meta-analysis approach. Target length: 15-20 pages." > behaviors/default.txt
```

---

### Why the Behavior File Matters

Unlike the outline (which organizes content) or the literature review (which frames the context), the behavior file **establishes the research style and approach**. It ensures the AI aligns with your academic expectations, helping it produce content that matches your intended **tone** and **structure**.

## Step 3: Generate the Outline

A well-defined outline provides the structure for a coherent paper, helping maintain focus and clarity. Let's build an outline for your academic paper.

1. **General Outline**:

   ```
   papercraftr outline general-outline "Summarize the key contributions of a paper exploring the connection between AI models and cognitive psychology, with a focus on systematic review findings."
   ```

2. **Section Summaries**:

   ```
   papercraftr outline section-summary "Summarize the introduction, methodology, results, and discussion sections for a paper exploring AI's impact on cognitive psychology."
   ```

3. **Key Points**:

   ```
   papercraftr outline key-points "Identify the main points to address in a systematic review on the applications of AI in cognitive psychology."
   ```

4. **Detailed Synopsis**:

   ```
   papercraftr outline detailed-synopsis "Outline each section of a research paper that aims to evaluate AI's influence on cognitive processes, focusing on methodology and critical findings."
   ```

## Step 4: Organize Literature and Framework

A comprehensive **literature review** situates your research within the existing body of knowledge, highlighting its significance. Here's how you can organize and develop this part with PaperCraftr:

1. **Review Key Studies**:

   ```
   papercraftr organize_lit review "Review studies connecting neural networks with cognitive processes, focusing on key findings and identified research gaps."
   ```

2. **Conceptual Framework**:

   ```
   papercraftr organize_lit framework "Develop a conceptual framework that illustrates the interaction between AI and cognitive psychology."
   ```

3. **Identify Gaps**:

   ```
   papercraftr organize_lit identify-gaps "Identify unexplored areas within existing literature on AI's impact on memory and perception."
   ```

## Step 5: Draft Each Section

With a structured outline and literature review, we can now proceed to draft each section. PaperCraftr enables a systematic approach to academic writing.

1. **Draft Introduction**:

   ```
   papercraftr generate_section introduction "Write an introduction summarizing the relevance of AI in cognitive psychology, including research questions and hypotheses."
   ```

2. **Draft Methodology**:

   ```
   papercraftr generate_section methodology "Write the methodology section, detailing the systematic review approach used to analyze studies on AI and cognition."
   ```

3. **Draft Results**:

   ```
   papercraftr generate_section results "Summarize the findings, focusing on the impact of AI models on cognitive functions like memory and learning."
   ```

4. **Draft Discussion**:

   ```
   papercraftr generate_section discussion "Discuss the implications of AI in cognitive psychology, including potential applications and future research directions."
   ```

## Step 6: Refine and Finalize

**Iterate** over each draft to improve clarity and academic rigor, ensuring a consistent tone and quality throughout your paper.

1. **Consistency Check**:

   ```
   papercraftr iterate consistency-check "Ensure terminology and style are consistent across sections."
   ```

2. **Review References**:

   ```
   papercraftr references review "Organize and format references according to the target journal's citation style."
   ```

3. **Proofreading**:

   ```
   papercraftr iterate proofread "Check for grammar, clarity, and formatting across the entire paper."
   ```

4. **Generate PDF**:

   ```
   papercraftr publish pdf en
   ```

## Step 7: Chat with Your Assistant

PaperCraftr includes a command to chat directly with your AI assistant. This feature allows you to ask questions, refine ideas, or request improvements to your paper's content, all from the terminal.

### How to Start a Chat

To start chatting with your assistant, make sure your project is initialized and run:

```
papercraftr chat
```

### Example Chat Session

1. **Ask for section feedback**:

   ```
   [You]: "What are the strengths and weaknesses of the introduction section in my paper on AI in cognitive psychology?"
   ```

2. **Request writing help**:

   ```
   [You]: "Help me improve the clarity of the methods section."
   ```

---

Happy writing with **PaperCraftr**!
