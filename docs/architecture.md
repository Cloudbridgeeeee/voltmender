# Proposed AWS architecture

| Service | Role |
|---|---|
| IoT Core | Live readings from meters and sensors, read only |
| S3 and Lambda | Reading exports and work orders, checked as they arrive |
| SageMaker AI | Normal ranges and anomaly models per asset |
| Bedrock | Plain-language alert notes that cite readings and work orders |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
