LLM usage
***********

1. Which AI tool or LLM model did you use, and why did you choose it?

I used ChatGPT to help with the test plan and Claude for decoding Wireshark logs.
I chose Claude MCP for wireshark as it offered support for pcapng analysis and Chatgpt as a sparring partner to help structure the test plan, identify edge cases, and refine QA thinking.

2. How did you use it during the assignment?

ChatGPT was used to ensure completeness of QA coverage (risks, edge cases, scenarios), refine wordings for bug reports and testcases and to ensure that no major misses are there.In general, it was used to supplement my own findings. I also used chatgpt to support understanding of unfamiliar concepts while analyzing wireshark logs in assignment 3( as I am not from audio background). This helped me to understand log components and protocols, interpret interactions between devices and hence enabled me to decode the roles of each device and guide my analysis approach (what to look for, how to break down logs).

Claude was used to decode the wireshark logs from Assignment 2 as standard dissectors in wireshark did not give any meaningful insights.

3. Approximately how much time did you spend using it? 

Assignment 1: ~50%
Assignments 2 & 3: ~70% (primarily due to log analysis complexity)

4. Which part of your solution benefited the most from it?

It helped me to identify the edge case in feature testing. In wireshark analysis, it helped me understand the logs and decode each item.


5. What was the biggest drawback or limitation?

Biggest drawback was hallucinations and incorrect assumptions from LLMs, requiring our own judgment and domain knowledge to validate the output.

6. How did you validate the AI-generated output before submitting your final answer?

I usually correlate the output with what I know from my experience and what I can infer from the other sources. For eg, test plan was created using hints from LLM output but based on my experience from similar situations, I cross-checked against the feature requirements provided and ensured all expected behaviors were covered by tests. 
I formed my own hypotheses (especially for log analysis) and checked whether the AI suggestions aligned with observable data

7. Were there any suggestions from the AI tool that you decided not to use? Why?

Yes.

In Assignment 2, Claude’s interpretation relied on a parsing logic that remained unverified due to the lack of a vendor-specific log decoder. Hence, I treated the output as a possible hypothesis rather than a confirmed finding, as I could not independently validate its accuracy against available evidence

8. What part of the final submission best reflects your own independent reasoning?

Final test strategy and prioritization decisions, Risk assessment and release decisions, Interpretation and conclusions drawn from Wireshark logs, Decisions on which AI suggestions to accept or reject
AI was used as a supporting tool, while the final conclusions and decisions were based on my own judgment.
