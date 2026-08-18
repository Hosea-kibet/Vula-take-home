### RCA 

A bad major model deployment v1.3 was rolled out and carries has a huge latency.

## Supporting Evidence
 - **Every single v1.2 request is fast (90 - 120ms) and return status OK.**
 - **Every single v1.3 request is slow (680 - 890ms) it past the threshhold.**
 - **The mix of v1.2 and v1.3 responses in the same window shows that this is a canary/partial rollout.Traffic is split,all requests are not timing out.**


### Immediate Remediation
Traffic should be rolled back from v1.3 to the stable v1.2 model.

### Prevention

Load test models before before release.
On release allocate the new model with a small slice of traffic.
When latency threshold is breached rollback to the stable model.

### Retrospective Notes

v1.3 shipped with no latecy gate. Pre deploy bencmarking would have caught this.
A friday 6:30 is risky. Revist deploy-freeze windows.
Introduce alerts. The issud was noticed via a 200% spike implement alerting so that this can be picked early enough.
