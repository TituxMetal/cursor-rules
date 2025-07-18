# Cursor Editor Rules Library

This is a comprehensive collection of **Cursor Editor rules** designed to guide AI code generation,
enforce coding standards, and maintain architectural consistency across web development projects.
These rules can be used as a starting point for any web development project using Cursor Editor.

## Purpose

This rules library provides a solid foundation for:

- **New Projects:** Copy and customize these rules for your own web development projects
- **Consistency:** Ensure all projects follow the same architectural and coding standards
- **AI Guidance:** Help Cursor's AI understand your preferred patterns and generate code accordingly
- **Team Standards:** Share consistent rules across development teams

## Philosophy

- **AI-Guided Development:** Rules guide Cursor's AI to generate code that follows project standards
- **Context-Aware Application:** Rules are applied based on file types and project structure
- **Consistency Enforcement:** Every rule ensures all AI-generated code follows the same standards
- **Self-Documentation:** Rules are written in Markdown with clear descriptions for both humans and
  AI

## Folder Structure

- Rules are grouped by category in subfolders:
  - `00-architecture/` — System and code organization
  - `01-standards/` — Clean code, naming, and general standards
  - `02-programming-languages/` — Language-specific best practices
  - `03-frameworks-and-libraries/` — Framework/library usage (React, NestJS, MobX, etc.)
  - `04-tools-and-configurations/` — Tooling and package management
  - `05-workflows-and-processes/` — Development and debugging workflows
  - `06-templates-and-models/` — Code and documentation templates
  - `07-quality-assurance/` — Testing and QA standards
  - `08-domain-specific-rules/` — Business/domain-specific rules
  - `09-other/` — Miscellaneous

## Rule File Format

- Each rule is a `.mdc` Markdown file with a frontmatter header:
  - `description`: When and why to apply the rule
  - `globs`: File patterns where the rule applies
  - `alwaysApply`: If true, the rule is global
- Example:

  ```mdc
  ---
  description: Enforce Clean Architecture in backend
  globs: apps/backend/**, src/**/*.ts
  alwaysApply: false
  ---
  - Separate code by layer: Domain, Application, Infrastructure, Presentation
  - Direct dependencies inward only
  ...
  ```

## How Rules Are Applied

- **Glob Patterns:** Each rule specifies file patterns (e.g., `apps/frontend/**/*.tsx`) to target
  relevant code. Cursor's AI applies these rules contextually based on the current file.
- **alwaysApply:** If true, the rule is enforced globally across all files; otherwise, only in
  matching files.
- **AI-Readable Format:** Rules are written as concise, actionable commands that Cursor's AI can
  understand and follow.
- **Context-Aware:** Rules help Cursor understand when and how to apply specific coding patterns.

## Main Rule Categories (Summary)

- **Architecture:** Clean Architecture, feature-based frontend, modular backend
- **Standards:** Clean code, naming conventions, file/function size limits
- **Programming Languages:** TypeScript best practices, naming, typing
- **Frameworks/Libraries:** React, MobX, NestJS, React Router, Tailwind CSS
- **Tools/Config:** Yarn usage, package installation policies
- **Workflows:** Bug finding, process documentation
- **Quality Assurance:** Testing standards for unit, integration, frontend, backend

## Updating or Adding Rules

- Use the provided template in `meta-generator.mdc` for new rules
- Place new rules in the correct category folder
- Use clear, concise descriptions and actionable bullet points that Cursor's AI can understand
- Update glob patterns and `alwaysApply` as needed
- For major changes, review and update related rules for consistency

## Working with Cursor's AI

- These rules automatically guide Cursor's AI when generating code
- The AI will follow the applicable rules based on the current file context
- Rules help ensure generated code matches your project's architecture and standards
- When asking Cursor to generate code, it will reference these rules automatically

## Getting Started

1. **Copy the Rules:** Copy the `.cursor/rules` directory to your new project
2. **Customize:** Modify rules to match your project's specific needs and preferences
3. **Test:** Ask Cursor to generate code in your project to verify the rules work as expected
4. **Share:** Contribute improvements back to this library for the community

## Contributing

- Read all relevant rules before starting work
- When in doubt, check the `.cursor/rules` folder for guidance
- Propose rule changes via pull request, following the template
- Test rule changes by asking Cursor to generate code in relevant files
- Share your customizations that might benefit other developers

---

This documentation ensures that the Cursor Editor rules library remains transparent, maintainable,
and effective for AI-guided development across multiple projects.
