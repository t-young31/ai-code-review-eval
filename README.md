# ai-code-review-eval

## Hypothesis

Development velocity is enhanced by using a AI code review tool before creating a PR and there is a best option.

## Notes

- Best is a function of: {cost, accuracy, ease of use, execution time}.
- Models: Gemini 2.5, Claude X, OpenAPI Codex
- Running gemini with `gemini -s`
- Running codex with `codex --sandbox read-only --ask-for-approval on-request`
- Running claude with `claude --permission-mode plan`

## Results

- Accuracy is defined using correct over total suggestions.
- Overlap is number of suggestions that were the same as the human (my) review.
- Usefulness is a out of 5 and has no well defined meaning.

### https://github.com/ucl-arc-tre/portal/pull/453

1. Gemini 2.5. Accuracy: 2/2. Time: 2m. Overlap: 2/2. Usefulness: 5
1. Codex 5.2. Accuracy: 1.5/2. Time: 1m. Overlap: 1/2. Usefulness: 3
1. Claude Opus 4.5. Accuracy 5/8. Overlap 1/8. Usefulness: 2. Comment: `Error: File content (28937 tokens) exceeds maximum allowed tokens (25000). Please use offset and limit parameters to read specific portions of the file, or use the GrepTool to search for specific content.`

## Conclusion

<!--
Gemini/Claude/CodeRabbit/Copilot should/n't be used for code review
--->
