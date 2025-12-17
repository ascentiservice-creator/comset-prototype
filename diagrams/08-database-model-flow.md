# Database Logical Model

```mermaid
flowchart LR
  USER[User] --> COMSET[Comset]
  COMSET --> ITEM[Comset Item]

  COMSET --> STATUS[Comset Status]

  ITEM --> PRODUCT[Product]
  PRODUCT --> CATEGORY[Category]

  PRODUCT --> SPEC[Product Spec]

  USER --> ROLE[User Role]
