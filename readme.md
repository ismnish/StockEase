mermaid
erDiagram
    BUSINESS ||--o{ USER          : owns
    BUSINESS ||--o{ CATEGORY      : has
    BUSINESS ||--o{ SUPPLIER      : contracts
    BUSINESS ||--o{ PRODUCT       : lists
    BUSINESS ||--o{ PENDINGSTOCK  : includes

    USER  }o--|| BUSINESS         : belongs_to
    USER  ||--o{ PENDINGSTOCK     : creates
    
    CATEGORY ||--o{ PRODUCT        : groups

    SUPPLIER ||--o{ PRODUCT        : supplies
    SUPPLIER ||--o{ PENDINGSTOCK   : sends

    PRODUCT }o--|| CATEGORY
    PRODUCT }o--|| SUPPLIER

    PENDINGSTOCK }o--|| SUPPLIER
    PENDINGSTOCK }o--|| USER
    PENDINGSTOCK }o--|| BUSINESS
