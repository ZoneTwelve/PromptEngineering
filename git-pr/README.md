# git Pull Request Prompts

Inspired by [PR-Agent](https://github.com/Codium-ai/pr-agent)
I'm going to improve they's prompts.

## Code Review Prompts
Source: [pr_reviewer_prompts.toml](https://github.com/Codium-ai/pr-agent/tree/fed0ea349a3f4ad2f6164615862307bb0eef1acb)
Updated: [New PR Reviewer Prompt](./updated_system_prompt.txt)

### System

[System Prompt](./original_system_prompt.txt)

Details (original):
 - a template for the system prompt
 - include a list of files changed
 - outputs required a YAML schema

Changes:
 - Generalize
   - Remove the conditions
   - Remove the name of the reviewer
   - More flexible
   - Allow users to add additional fields or subsections that could capture more specific insights.

Recommand:
 - Don't use JSON to generate the output
 - If possible, consider simplifying some of the logic to make it more accessible.
 - Provide clearer explanations for the conditionals to ensure the user understands when each section should be included.


Differences:
  - Complexity: The original prompt is more complex and includes conditional logic, while the second prompt provides a simpler, fixed structure.
  - Content Focus: The original prompt includes a broader range of elements, such as scoring, testing, and focus, whereas the second prompt emphasizes general and specific code feedback, including security concerns.
  - Explanation: The original prompt includes more details on each field's purpose and gives specific guidance on what to avoid. The second prompt is more brief in its explanations.