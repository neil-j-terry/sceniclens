---
name: Memory
description: 
---
# Memory
## Use Cases
This memory system is used when an agent or prompt needs to maintain knowledge beyond a single task.
Typical uses include:
- Storing useful facts learned while working on tasks
- Remembering user preferences and working styles
- Recording domain knowledge that will help future reasoning
- Capturing tool usage patterns, commands, or configurations
- Maintaining consistent context across multiple sessions
- The memory database acts as a structured knowledge base that improves reasoning and decision making over time.
- The system should store only reusable knowledge, not temporary conversation context.

## Task
Maintain a structured memory system rooted in the database specified when this skill is referenced.

The memory system should act as a persistent knowledge layer that improves future tasks.

The agent must:
- Read memory when beginning work
- Use memory to inform reasoning when relevant
- Write new knowledge when something valuable is learned
- Maintain the memory repository to ensure quality and structure

The memory database should remain concise, organised, and high signal.
## Instructions

Tag each item of memory with the following.
﻿﻿general - cross-project facts, preferences, environment setup
﻿﻿domain | {topic} - domain-specific knowledge (one record per topic)
﻿﻿tools | {tool) - tool configs, CLI patterns, workarounds (one record per tool)


When I say "reorganize memory":
- Read all memory records
- Remove duplicates and outdated entries
- Merge entries that belong together
- Split records that cover too many topics
- Show me a summary of what changed

### Input
The database used to store memory records.
This database must be read at the start of a session when the memory skill is used.
All memory entries must be written to this database.

### Rules

- When learning information worth remembering, immediately store it in the memory repository.
- Memory should only contain knowledge that will be useful again in future tasks.
- Memory entries must remain small, focused units of knowledge.
- Each memory item must contain only:
    - What
    - Why
- Before writing a new memory record:
    - Search the memory database for similar entries
    - Update an existing entry if the information overlaps
    - Create a new record only if the knowledge is distinct

- If a memory entry contains multiple ideas, split it into separate records.
- If a memory entry becomes outdated or incorrect, update or remove it.

- When performing a task:
    - Read the memory database
    - Identify relevant records
    - Use them as supporting context
Memory should guide reasoning but must not override direct user instructions.

### Memory Tags
Each memory record must be tagged with one of the following categories.
general
Cross project knowledge, user preferences, environment setup.
domain | {topic}
Knowledge specific to a subject or discipline. One record per topic.
tools | {tool}
Tool configuration, usage patterns, commands, or workarounds.

Examples of tags:
general
domain | advertising
tools | notion

### Confidence
Each memory record must include a confidence level indicating how reliable the knowledge is.
Confidence helps agents decide how strongly to rely on the memory.
Confidence levels:
- High
    - Confirmed fact, repeated behaviour, or direct user statement.
- Medium
    - Likely true but based on limited evidence or inference.
- Low
    - Initial observation or assumption that may change.

Rules for assigning confidence:
- Use High confidence when the information is confirmed by the user or repeatedly observed.
- Use Medium confidence when the information is likely correct but not yet confirmed.
- Use Low confidence when the information is based on a single observation or assumption.

When updating memory:
- Confidence should increase if the knowledge is repeatedly confirmed.
- Confidence should decrease or be removed if the knowledge becomes outdated or contradicted.
- Agents should prioritise High confidence records when retrieving memory.

### Memory Maintenance
- When the command "reorganise memory" is given:
    - Read all memory records
    - Remove duplicates
    - Merge related entries
    - Split entries covering multiple topics
    - Remove outdated information
    - Ensure all records follow the correct structure
- Then produce a short summary showing:
    - records removed
    - records merged
    - records updated
    - records created

### Format to Follow
Each memory record must follow this structure.

Tag
[tag name]

What
- Clear description of the knowledge to remember.

Why
- Explanation of why this knowledge is useful in future tasks.

Each record must contain one clear idea only.
## Examples
### Example 1
Tag
- general

What
- The user prefers clear writing with simple language and short paragraphs.
Why
- Responses should match the user's communication style.

### Example 2
Tag
- domain | advertising_testing

What
- System1 evaluates advertising effectiveness using metrics including Star Rating, Spike, Fluency, and Fast Fluency.

Why
- Understanding these metrics is required when analysing Test Your Ad outputs.

### Example 3
Tag
- tools | notion

What
- Notion databases are used to store competitive intelligence and structured research.

Why
- Agents should structure insights so they can be easily stored in Notion.

## Common Pitfalls
- Avoid storing temporary context.
- Avoid storing full conversations.
- Avoid duplicating existing records.
- Avoid vague or unclear knowledge entries.
- Avoid storing information that will not be useful again.
- Memory should behave as a structured knowledge system rather than a conversation log.


