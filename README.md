# ecs_hands_on
AWS コンテナ設計・構築入門

## ネットワークの構築

### サブネットごとのIPv4 CIDRブロック

| 用途 | NW区分 | AZ | CIDR | サブネット名（名前タグ） |
| --- | --- | --- | --- | --- |
| Ingress      | Public  | 1a | 10.0.0.0/24   | sbcntr-subnet-public-ingress-1a |
|              | Public  | 1c | 10.0.1.0/24   | sbcntr-subnet-public-ingress-1c |
| Application  | Private | 1a | 10.0.8.0/24   | sbcntr-subnet-private-container-1a |
|              | Private | 1c | 10.0.9.0/24   | sbcntr-subnet-private-container-1c |
| DB           | Private | 1a | 10.0.16.0/24  | sbcntr-subnet-private-db-1a |
|              | Private | 1c | 10.0.17.0/24  | sbcntr-subnet-private-db-1c |
| Admin        | Public  | 1a | 10.0.240.0/24 | sbcntr-subnet-public-management-1a |
| Admin(spare) | Public  | 1c | 10.0.241.0/24 | sbcntr-subnet-public-management-1c |
