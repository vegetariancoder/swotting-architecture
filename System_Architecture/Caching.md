# Overview of Caching

- **Caching** brings data closer to the user, improving retrieval speed.
- Examples include:
  - **Web Browser Cache**: Stores webpages locally to improve load times.
  - **Service Cache**: Reduces retrieval times by storing data closer to the business logic, bypassing repeated database queries.

## How Caching Works in Applications

- **Cache layers** are typically placed between the database and the business logic layer.
- Data is stored in memory, allowing fast access and reducing the load on the database.
- **Performance Trade-Off**: Caches enhance speed but may lose data in the event of a crash, as data in memory is less reliable than disk-based storage.

## When to Use Caching

- Cache frequently accessed, infrequently modified data.
  - **Benefits**: Reduces system load, optimizes user experience.
  - **Challenges**: Keeping cache synchronized with the central data source.

## Types of Caches

### 1. In-Memory, In-Process Cache
- Integrated directly into the service’s memory.
- **Advantages**:
  - High performance, as data retrieval is internal to the service.
  - Simplified setup using in-language libraries.
- **Limitations**:
  - Limited storage size (dependent on server memory).
  - Unsuitable for scenarios requiring data distribution across servers.

### 2. Distributed Cache
- A standalone product accessible across multiple servers.
- **Advantages**:
  - Larger storage capacity, distributed across multiple nodes.
  - Built-in synchronization ensures all nodes have consistent data.
- **Limitations**:
  - Slightly slower due to network latency and serialization.
  - Limited to primitive data types (e.g., strings, numbers).

## Choosing a Cache Strategy

- **Distributed Cache**:
  - Ideal when data needs to be shared across servers.
  - Best for large-scale applications with high failover and storage requirements.
- **In-Memory, In-Process Cache**:
  - Optimal when performance is critical and complex data structures are used.
  - Suitable for single-server setups or when distribution is unnecessary.

## Summary

- Effective caching depends on the frequency of data access and modification.
- Use **distributed cache** for scalable, synchronized data across servers.
- Use **in-memory, in-process cache** for highest speed and complex data structures.
- Design caching to enhance performance without overloading or desynchronizing the system.
