# Database Design

## Main Tables

### Users

* user_id
* name
* email
* password
* role

### Laptop Models

* laptop_id
* model_name
* processor
* RAM
* storage
* operating_system
* price

### Laptop Requests

* request_id
* user_id
* laptop_id
* reason
* request_date
* status

### Approvals

* approval_id
* request_id
* manager_id
* approval_status
* comments
* approval_date

### Procurement Orders

* order_id
* request_id
* vendor
* order_date
* delivery_date
* order_status

## Relationship

Users submit Laptop Requests.

Laptop Requests refer to Laptop Models.

Managers review Laptop Requests.

Approved requests are converted into Procurement Orders.
