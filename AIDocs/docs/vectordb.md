# Vector DB state in 2025 and a small comparison
Here’s a quick comparison table of popular vector databases, comparing their suitability for quick prototyping and enterprise-level scalability, along with other core features like ease of use, ecosystem, and cloud/on-prem support:

| Vector DB          | Quick Prototyping     | Enterprise Scalability       | Open Source | Cloud Managed  | Language Support       | Notable Features / Pros                       | Limitations                            |
| ------------------ | --------------------- | ---------------------------- | ----------- | -------------- | ---------------------- | --------------------------------------------- | -------------------------------------- |
| **Pinecone**       | ✅ Excellent           | ✅ Very good                  | ❌ Closed    | ✅ Yes          | Python, JS, REST API   | Fully managed, easy to use, high availability | No self-hosted/on-prem version         |
| **Weaviate**       | ✅ Great               | ✅ Excellent                  | ✅ Yes       | ✅ Yes          | Python, Go, REST       | Built-in ML models, hybrid search             | More complex ops for self-hosting      |
| **Milvus**         | ✅ Good                | ✅ Excellent                  | ✅ Yes       | ✅ Zilliz       | Python, Java, Go, REST | Highly scalable, GPU support                  | Slightly steep learning curve          |
| **Qdrant**         | ✅ Great               | ✅ Very good                  | ✅ Yes       | ✅ Qdrant Cloud | Python, Rust, REST     | Fast, lightweight, simple REST API            | Young compared to Milvus/Weaviate      |
| **FAISS**          | ⚠️ Manual effort      | ⚠️ Limited (not DB)          | ✅ Yes       | ❌ No           | Python, C++            | Highly performant for similarity search       | Not a full DB, no persistence          |
| **Redis (Vector)** | ✅ Easy                | ✅ Good (w/ Redis Enterprise) | ✅ Yes       | ✅ Yes          | Many (via clients)     | Multi-purpose DB, easy to integrate           | Basic vector features, not specialized |
| **Chroma**         | ✅ Great (LLM-focused) | ⚠️ Early stage               | ✅ Yes       | ❌ No           | Python                 | Built for LLM apps, easy to use               | Not enterprise ready yet               |
| **Vald**           | ⚠️ Less friendly      | ✅ Good (K8s native)          | ✅ Yes       | ❌ No           | gRPC, Go, Python       | Kubernetes native, ANN via NGT                | Complex deployment                     |

- Best for Prototyping: Chroma, Qdrant, Weaviate, Pinecone

- Best for Enterprise: Weaviate, Milvus, Pinecone

- Fully Managed (Cloud): Pinecone, Weaviate, Qdrant Cloud

- Self-hostable & Open Source: Weaviate, Milvus, Qdrant, Redis, Vald

We will be evaluating Weaviate to see how easy it is to setup. May switch to Pinecone later.