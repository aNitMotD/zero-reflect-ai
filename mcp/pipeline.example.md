# Example MCP Pipeline with ZR Gate

1. User submits input
2. Trigger check (T1–T5)
3. If triggered → invoke ZR
4. Apply gates (G1–G5)
5. If allowed → execute downstream tools
6. Otherwise → return ZR output and stop

> Note:
> This pipeline does not perform decision-making or responsibility transfer.
> Downstream execution must not be interpreted as automated judgment.
> All triggers, inputs, and execution contexts remain under explicit human responsibility.
