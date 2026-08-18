# Architecture Notes: Human-in-the-Loop AI Review Portal

## Pipeline

```text
AI Output Queue -> Reviewer Assignment -> Review UI (Accept/Reject/Rate/Comment) -> Analytics
```

## Components

- Conversation review queue
- AI summary review
- Accept / reject actions
- Quality rating
- Reviewer comments
- Error categorization/taxonomy
- Reviewer assignment
- Role and group-based permissions
- Review analytics dashboard
- Large-dataset streaming and export

## Design Notes

- Keep provider/model choices swappable behind interfaces (see `multi-llm-router`
  and similar projects in this portfolio for the general pattern).
- Prefer configuration-driven pipelines (YAML/JSON in `configs/`) over hardcoded
  parameters so experiments are reproducible.
