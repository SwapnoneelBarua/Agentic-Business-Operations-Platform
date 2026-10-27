# Security

This scaffold does not yet implement authentication, authorization, tenant isolation, or production secrets management. Do not expose it to untrusted networks or use it with real customer data until those controls are implemented and reviewed.

Agent-initiated external actions should require explicit human approval. Keep credentials out of source control and use environment-specific secret storage outside local development.
