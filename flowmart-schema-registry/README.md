# FlowMart Schema Registry

This repository serves as a demo schema registry for a fictional e-commerce application called "FlowMart". It showcases how an organization might use a Git repository to manage and version various data schemas (JSON Schema, Avro, Protobuf) across different domains and services.

## Purpose

The primary goal is to provide a tangible example of a schema registry structure that is:

*   **Understandable:** Easy to navigate and comprehend.
*   **Commonly Used:** Reflects patterns seen in organizations using Git for schema management.
*   **Illustrative:** Contains a variety of schema types and examples relevant to an e-commerce context.

## Structure

The schemas are organized primarily by **domains**. Each domain represents a distinct area of the e-commerce business.

```
flowmart-schema-registry/
├── README.md
└── domains/
    ├── products/
    │   └── schemas/
    │       ├── product_v1.json
    │       ├── product_created_v1.avsc
    │       ├── product_updated_v1.proto
    │       ├── product_viewed_v1.json
    │       └── category_v1.json
    ├── orders/
    │   └── schemas/
    │       ├── order_v1.json
    │       ├── order_item_v1.json
    │       ├── order_created_v1.avsc
    │       ├── order_shipped_v1.proto
    │       └── order_cancelled_v1.json
    ├── users/
    │   └── schemas/
    │       ├── user_v1.json
    │       ├── address_v1.json
    │       ├── user_registered_v1.avsc
    │       └── user_profile_updated_v1.proto
    ├── payments/
    │   └── schemas/
    │       ├── payment_v1.json
    │       ├── payment_processed_v1.avsc
    │       └── payment_failed_v1.proto
    └── inventory/
        └── schemas/
            ├── stock_item_v1.json
            ├── stock_level_updated_v1.avsc
            └── out_of_stock_alert_v1.proto
```

### Domains

*   **products:** Schemas related to product information, categories, and product-related events.
*   **orders:** Schemas concerning customer orders, order items, and order lifecycle events.
*   **users:** Schemas for user profiles, addresses, and user-related events.
*   **payments:** Schemas detailing payment transactions and payment status events.
*   **inventory:** Schemas for managing stock levels and inventory-related events.

### Schema Types

This registry includes examples of:

*   **JSON Schema (.json):** For defining the structure of JSON data.
*   **Apache Avro (.avsc):** A schema definition language for Avro, a data serialization system.
*   **Protocol Buffers (.proto):** Google's language-neutral, platform-neutral, extensible mechanism for serializing structured data.

## How to Use

This repository is for demonstration purposes. In a real-world scenario:

*   Schemas would be more detailed and comprehensive.
*   CI/CD pipelines would be set up for schema validation and evolution.
*   Tooling might be used to generate code from these schemas or to integrate with a schema registry service (like Confluent Schema Registry, AWS Glue Schema Registry, etc., even if the source of truth is Git).

Feel free to explore the schemas and use this structure as inspiration for your own projects. 