# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built:disruption-care chat agent for Larkspur; multi-tool loop on the Messages API; 9 given tools + MCP
Does:looks up booking → checks flight status → resolves policy → tells the customer their options (rebook / refund / vouchers / escalate)
Number:~2,927 tokens per turn just for tool schemas (next_available_day (495) and fare_rules (297))
Guardrail:confirm_rebooking is irreversible and needs a customer-click token the agent can't forge — chat "yes" doesn't count
Next:only send the tools a case actually needs, instead of all 11 every turn
Still broken:abusive ticket (R8KD3F) gets a calm, normal reply, no tone handling at all
Lever: cost

## Priya asked

Costs: ~2,927 tokens/turn in tool schemas
Wrong:it could quote the wrong policy, or act without the customer's confirmation
Runs it:the agent handles routine disruptions; humans take escalations (groups, refunds, minors)
Left out: tone on abusive messages; multi-passenger capacity
