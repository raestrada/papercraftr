## Advanced Usage of PaperCraftr

PaperCraftr provides advanced features for users who want more control over how the tool interacts with their projects. This guide will walk you through these features, including multi-prompt responses, file backups, and the `reload-files` command.

### Multiple Prompts Feature

By default, PaperCraftr uses **multiple prompts** when generating or refining content. This feature allows for more detailed and comprehensive outputs by breaking the response into parts and requesting confirmation before continuing. If you prefer a single, uninterrupted response, you can disable this feature by editing the `Papercraftr.json` configuration file.

In your `papercraftr.json` file:

```json
{
  "multiple_answer": false
}
```

With `multiple_answer` set to `false`, PaperCraftr will generate a single, complete response for any prompt, without dividing it into sections.

### Backup Files

PaperCraftr automatically creates backups of any files it modifies. These backup files have a `.back` extension and are created in the same directory as the original file. This feature ensures that you always have a copy of your previous work and can easily revert to a previous state if needed.

For example, if you run a command to generate or refine a chapter, PaperCraftr will create a backup of the current file before making any changes:

```
chapters/chapter_1.md
chapters/chapter_1.md.back
```

The backup file allows you to compare the before and after states or recover content if needed.

### Reload Files with `Papercraftr reload-files`

The **`reload-files`** command is a powerful feature that allows you to synchronize your local content with the retrieval system used by PaperCraftr. This ensures that any recent changes you've made are correctly picked up by the assistant, enhancing its understanding of your story before you execute additional commands.

#### Example Usage:

```bash
Papercraftr reload-files --book-path "path/to/your/book"
```

This command will:

- **Re-sync all content**: It updates the assistant's context to reflect any new or edited content in your project.
- **Overwrite current agent files**: All agent files will be overwritten, ensuring the latest versions are used for retrieval during prompts.

### When to Use `reload-files`

- **After Manual Edits**: If you've made manual changes to the markdown files within your book project, use `reload-files` to ensure these changes are understood by PaperCraftr before running new commands.
- **After Deleting Content**: If you delete any sections or chapters, running `reload-files` will help PaperCraftr adapt to the new structure of your project, avoiding references to content that no longer exists.

### Summary

- **Multiple Prompts**: Enabled by default, but can be turned off for a single-response output.
- **Backup Files**: Automatically generated with a `.back` extension for every modified file.
- **Reload Files**: Use `Papercraftr reload-files` to update the assistant's context after making manual changes.
- **Custom Sections**: Create custom sections between methodology and results with specified order numbers.

These advanced features provide greater control over your workflow and ensure that your project evolves smoothly and consistently.

### Custom Sections

PaperCraftr allows you to create custom sections between the methodology and results sections of your paper. This is useful for papers that require additional sections like theoretical frameworks, data collection details, or specialized analyses.

#### Creating Custom Sections

To create a custom section, use the `custom` command with the `--order` option to specify its position:

```bash
papercraftr generate_section custom --order 1 "Theoretical Framework" "Develop a theoretical framework that connects AI models with cognitive processes."
```

The `--order` parameter determines the sequence of custom sections. For example:
- `--order 1` places the section immediately after methodology
- `--order 2` places it after the first custom section
- And so on...

#### File Naming Convention

Custom sections are saved with filenames that include their order number and title:

```
sections/custom_1_theoretical_framework.md
sections/custom_2_data_collection.md
```

This naming convention ensures that sections are processed in the correct order when generating the final PDF.

#### Refining Custom Sections

You can refine custom sections just like any other section:

```bash
papercraftr generate_section custom --order 1 "Theoretical Framework" "Add more details about the connection between neural networks and memory processes."
```

The system will recognize the existing section and refine it rather than creating a new one.
