# Topic rotation (SAP-C02)

Cycle in this order. Skip a slot only if that exact topic+angle already appears in Linear/Docs; pick the next unused slot.

1. Scalability
2. High availability / DR
3. Microservices
4. Databases (SQL / NoSQL / caching)
5. Messaging / queues
6. Networking / VPC
7. Security / IAM
8. Cost optimization
9. Migration strategy
10. Multi-region
11. Serverless
12. Storage tiering

After a full cycle, start again with a harder angle (new constraints, failure modes, or SAP-C02 exam-style distractors).

## Difficulty bands

| Days | Focus |
|------|-------|
| 1–14 | Fundamentals: CAP, load balancing, sharding, caches, queues, basic HA |
| 15–35 | AWS-native: specific services, Well-Architected trade-offs, SAP-C02 scenarios |
| 36–56 | Mock interview: multi-constraint (scale + cost + compliance + DR) |

## Angle ideas (optional prompts when inventing the scenario)

- Scalability: flash-sale traffic, hot keys, write amplification
- HA/DR: RPO/RTO targets, multi-AZ vs multi-region, failover runbooks
- Microservices: service boundaries, saga vs choreography, blast radius
- Databases: read replicas, DynamoDB vs Aurora, cache invalidation
- Messaging: at-least-once, ordering, DLQs, backpressure
- Networking: private subnets, PrivateLink, hybrid connectivity
- Security: least privilege, encryption, zero-trust edges
- Cost: right-sizing, Spot, storage classes, reserved capacity
- Migration: 6Rs, dual-write, cutover risk
- Multi-region: active-active vs active-passive, conflict resolution
- Serverless: cold starts, concurrency limits, event fan-out
- Storage: lifecycle policies, Glacier retrieval, throughput vs cost
