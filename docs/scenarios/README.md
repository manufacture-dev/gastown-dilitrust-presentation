# Talk Scenarios

This directory contains scenario runbooks for public Gastown presentation flows.

Each scenario should:

- map to a talk definition in `talks/*.json`;
- reference the named prompt selected by that talk;
- separate the public narrative from operational setup details as much as possible;

## Scenarios

- `dilitrust-techday.md`: DiliTrust TechDay.
- `dev-with-ai-live-4.md`: Dev With AI Live #4.

## Prompt Convention

Talk prompts live in `public/prompts` and follow this pattern:

```text
gastown-demo-prompt.<prompt>.<locale>.txt
```

The prompt name comes from the talk JSON `prompt` field.
