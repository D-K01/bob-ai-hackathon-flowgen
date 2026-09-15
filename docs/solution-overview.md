# Solution Overview

## What We Built

We Built Flowgen AI which alerts Pune Municipal Corporation about any leaks or contamination in the water with the help of various sensors. Then an operator will assign a crew member to repair the said issue. The crew member will receive notification of task and complete details about it with location of the pipe which has faced the issue.

## How It Works

1. Pipe has some sort of leak / contamination.
2. the sensors send data to the dashboard at PMC.
3. Operator Assigns the issue to a crew member.
4. Crew member gets the details about the problem.
5. Crew member fixes the task and marks the task as completed.
6. The issue is shown as resolved in the dashboard.

## Architecture Diagram

> See [`architecture.md`](architecture.md) for the detailed diagram.

[Optionally include a simple ASCII or Mermaid diagram here for quick reference.]

```
[Sensor] → [Frontend: React] → [API: FastAPI] → [watsonx.ai] → [Dashboard]
                                    ↓
                             [PostgreSQL DB]
```

## Key Design Decisions

| Decision | Rationale |
|---|---|
|  Used watsonx.ai for anomaly detection |  Pre-trained models reduced time-to-value vs. building from scratch |

## IBM Technologies Used


- **IBM Tech 1 watsonx.ai:** "Used the `ibm/granite-13b-instruct-v2` model via the Python SDK to classify anomaly types from log text."
  
