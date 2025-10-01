Analyze these execution logs to determine if the test was successful.

TEST OBJECTIVE:
{test_objective}

WORKFLOW TYPE: {workflow_type}

{original_instructions_section}{code_section}EXECUTION LOGS:
{logs}

Please analyze these logs and determine:
1. Was the test successful? (YES/NO)
2. What is your confidence level? (HIGH/MEDIUM/LOW)
3. What key indicators led to your conclusion?
4. Provide a brief reasoning for your determination
5. If unsuccessful, what recommendation do you have?

IMPORTANT: You must provide a structured JSON response with the following format:
{{
    "success": true/false,
    "confidence": "high/medium/low",
    "reasoning": "Brief explanation of your determination",
    "key_indicators": ["indicator1", "indicator2", ...],
    "recommendation": "Optional recommendation if test failed"
}}

Focus on understanding the actual behavior, not just looking for error keywords. For example:
- If data was successfully retrieved/processed, it's likely successful even without explicit success messages
- If the code achieved its objective (e.g., fetched data, connected to service), consider it successful
- Look for patterns indicating normal operation vs actual failures