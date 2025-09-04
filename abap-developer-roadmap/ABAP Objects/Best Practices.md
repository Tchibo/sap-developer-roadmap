#Intermediate 

For ABAP OO, as for all coding paradigms, the main goal is to create understandable code that can be maintained and enhanced easily. ABAP code often remains in production longer than most other software, which makes writing good code even more important.

Here are some best practices specific to ABAP OO:

> [!toDo] A few more words about reuse
> Rather than subtopic 're-usable standard classes' mention XCO and ALV for reuse here.

- Do not reinvent the wheel: If SAP provides a framework that fits your use case, prefer it over custom implementations.
- Maintainability over performance: Use efficient constructs, but don’t over-optimize. The last few % of performance rarely justify added complexity and risk of bugs.
- Use comments to explain _why_, not _what_.
- Document methods and variables with ABAP Doc.
- Avoid deep inheritance. Complex hierarchies are confusing; prefer patterns like decorator.
- Leverage ABAP’s strengths: Internal Tables are powerful. Learn their details and how to apply them effectively (e.g., the different variants of ``LOOP AT itab``).
- Follow Clean ABAP, but stay pragmatic: extreme "Clean Code" can overcomplicate simple problems.

# Resources
#website [Clean ABAP](https://github.com/SAP/styleguides/blob/main/clean-abap/CleanABAP.md)