# InstagramPostingLlm Crew

InstagramPostingLlm is agentic LLM system prototype that will create engaging instagram posts for creators.

The system consists of 4 agents integrated together with the use of crewai framework flow:

### Planner Agent 

This agent will use a prompt like, "Create a content plan for an engaging Instagram post about bass guitar players." The output will be a detailed plan outlining the key points and visuals to be included in the post.

### Researcher Agent

This agent can be used to gather information about bass guitar players. We use google Serper search tool to search the web

### Writer Agent

This agent will use the output from the Planner Agent and the Researcher Agent to generate the Instagram post text. The prompt could be, "Write an engaging Instagram post about bass guitar players based on the following plan and research: [plan and research]."

### Photographer Agent

This agent will generate prompts for image generation. We use DALL E AI API to generate images based on these prompts. The prompts could be derived from the content plan and research.

### Instagram Post Workflow

We use crewai library's crew toolkit to create a workflow that integrates the agents. This workflow will take a topic as input, use the Planner Agent to create a content plan, use the Researcher Agent to gather information, use the Writer Agent to generate the post text, use the Photographer Agent to generate images, and finally, return the post text and images.
