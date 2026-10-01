# Evidence Notes

## Verified in the assessment

- Retell **Settings → Webhooks** was configured with the Webhook.site endpoint.
- Retell's **Test** action delivered an HTTPS POST to Webhook.site.
- The observed event was `call_started`.
- The observed call type was `web_call`.
- The observed status was `ongoing`.
- The request used `Content-Type: application/json`.
- The request included an `x-retell-signature` header.
- The observed start-event cost object showed `combined_cost: 0`.

## Evidence boundary

The captured webhook-test payload is a **start-event web-call payload**. It does not by itself prove that transcript, recording URL, duration, or final cost were received after a completed call.

Those fields should only be marked as completed evidence when a post-call `call_ended` or `call_analyzed` payload visibly contains them.

## Scope

Topic 5 uses the Retell Playground/Test Audio flow. A purchased phone number is not required for this webhook assessment flow.

## Links

- Loom: https://www.loom.com/share/08b977186d4b416b85740f966de3d9a7
- Webhook receiver: https://webhook.site/5f95e2c4-87d3-4114-bf4a-5d9bdb540666
- Repository: https://github.com/shaikshahid777/retell-ai-topic-5-webhooks-call-lifecycle-events
