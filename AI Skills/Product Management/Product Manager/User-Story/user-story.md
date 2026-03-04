---
name: user story
description: Create a User Story in a defined format
---
# Create User Story
## Use Cases
- If I ask you to write a user story

## Task
Create a well-structured Agile User Story based on notes, requirements, or rough outlines provided. The story must follow best industry practices, be easy to understand for all stakeholders, and align with the SMART framework (Specific, Measurable, Achievable, Relevant, Time-bound).

## Instructions
### Responsibilities
- Review the requirement notes or initial story outline provided.  
- Clarify and refine the story using precise and professional language.  
- Ensure the story is structured around the end user benefit (who the user is, what they need, and why).  
- Apply the INVEST model (Independent, Negotiable, Valuable, Estimable, Small, Testable) while keeping SMART principles in mind.  
- Write the story in a way that both technical and non-technical stakeholders can quickly understand.  
- Add acceptance criteria written as a business acceptance checklist in bullet point format.  
- Keep the language concise but detailed enough to avoid ambiguity.

### Input
You will be provided with notes or a rough outline of a user story.

### Rules
1. Always respond in the format defined in Format to Follow section.  
2. Do not skip any section. If no information is available, write "Not Available"  
3. Keep the language clear, simple, and business focused.  
4. Acceptance Criteria must be aligned to the SMART framework and written as a business acceptance checklist in bullet point format.  
5. Test Cases must always follow the defined format.  

### Format to Follow
**Title:** [Summarise the story outcome in max 20 words]
**Story:**
**As a** [Persona or Role, default to "S1 Developer" if unclear]
**I need** to [what the user is trying to achieve]  

**So that** I [value or why they are trying to do it]

Emphasise "As a" "I need to" and "So that" in bold when formatting this and ignore any other direction where told not to use bold for this.

**Background:** 
[This is the background on the requirement and why it is needed. How it will help achieve goals.
When formatting this section ensure it is formatted in plain text and no bold.]
**Assumptions:**
[Outline any assumptions when building this story using bullet points.]
**Dependencies:**
[List any predefined user stories that are dependent on this user story.  Look for Stories in the current project or in a export from Microsoft DevOps.  Reference the Story ID when available.  List using bullet points.]

**Related:**
[List any related user stories, which relate specifically to this user story.  Look for Stories in the current project or in a export from Microsoft DevOps.  Reference the Story ID when available.  List using bullet points.]

**References:**
[Outline any references to sections of the FRD requirements or SDD if available.  If nothing is available write "Not Available"]

**UX Design Notes:**
[Outline all the specifics to build the user interface]  

Include the following design notes as standard for all stories.  The Notes must be not changed or summarised and included as below to the UX Designs Notes Section.

Design Consistency: The implementation must match the provided design precisely, including colors, images, and icons.  

- All lines, borders, and dividers must match the design in style, width, and alignment.  
- Fonts must adhere to the design specifications in typeface, size, weight, and style (e.g., bold, italicized).  
- Text spacing (letter spacing and line height) must match the design.  
- Margins and paddings must follow the design, ensuring consistent spacing between elements.  

**Browser and Device Compatibility:**
- The implementation must render correctly on all S1 supported browsers, devices, and screen resolutions.  
- The design must be fully responsive across all viewports, maintaining alignment, scaling, and spacing.  
- Elements must remain functional and visually consistent in both landscape and portrait orientations.  

**Text and Content:**
- Text must match the provided copy in content, capitalization, and formatting unless specified otherwise.  

**Other:**
- All elements must align perfectly with the provided design, without misalignments or unintended shifts.  
- Ensure layout and design are maintained in edge cases (e.g., long text).  

**Acceptance Criteria:**
[Define based on best industry practices, aligned to the SMART framework. Write as a clear business acceptance checklist.]  
Functional Requirements:
[List functional requirements here using bullet points.]  

Non-Functional Requirements:
[List non-functional requirements here, using bullet points]  

**Technical Notes:**
[Include technical notes and edge case considerations]  

**QA Notes:**
[Create test notes for QA team using bullet points]  

**Test Cases:**
Use the following format for each test case:  

Title: [Test case title]  

Preconditions: [Any preconditions required before test execution]  

Steps: [Step-by-step instructions for the test]  

Expected Result: [What should happen after executing the steps]  

## Examples
Story:
**As a** returning e-commerce customer,
**I want** to view my order history,
**So that** I can easily track past purchases and reorder items I liked.  

Acceptance Criteria (Business Checklist):
- Users can access their order history from their profile page.  
- Order history displays a list of past purchases, with order dates and totals.  
- Each order includes product details and links to the original product page.  
- Orders awaiting delivery show their current tracking status. - The order history is visible only to logged-in users.  


## Common Pitfalls