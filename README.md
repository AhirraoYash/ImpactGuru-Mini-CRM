# ImpactGuru-Mini-CRM
 
Project Structure

ImpactGuru-Mini-CRM/
│
├── 📂 app/
│   ├── 📂 Http/
│   │   ├── 📂 Controllers/         <-- THE BRAIN (Handles logic)
│   │   │   ├── Auth/               (Login logic - Breeze will make this)
│   │   │   ├── CustomerController.php  (New: Logic for adding/editing customers)
│   │   │   ├── OrderController.php     (New: Logic for orders)
│   │   │   ├── DashboardController.php (New: For Admin/Staff stats)
│   │   │   └── Api/                    (New: For your REST API logic)
│   │   │
│   │   ├── 📂 Middleware/          <-- THE SECURITY GUARD
│   │   │   └── RoleMiddleware.php      (New: Checks if user is Admin or Staff)
│   │   │
│   │   └── 📂 Requests/            <-- THE VALIDATOR (Industrial Standard)
│   │       │   (We do NOT validate inside Controllers. We do it here.)
│   │       ├── StoreCustomerRequest.php
│   │       └── StoreOrderRequest.php
│   │
│   └── 📂 Models/                  <-- THE DATA REPRESENTATION
│       ├── User.php                (Exists: Employees)
│       ├── Customer.php            (New: Customer data)
│       └── Order.php               (New: Order data)
│
├── 📂 database/
│   ├── 📂 migrations/              <-- THE BLUEPRINTS (Table structure)
│   │   ├── ...create_users_table.php
│   │   ├── ...create_customers_table.php
│   │   └── ...create_orders_table.php
│   │
│   └── 📂 seeders/                 <-- FAKE DATA
│       └── DatabaseSeeder.php      (To create a fake Admin user for testing)
│
├── 📂 routes/
│   ├── api.php                     (For the Mobile App/REST API)
│   └── web.php                     (For the Website/Dashboard)
│
└── 📂 resources/
    └── 📂 views/                   <-- THE FRONTEND (Blade Files)
        ├── 📂 layouts/             (Master design)
        ├── 📂 customers/           (index.blade.php, create.blade.php)
        ├── 📂 orders/              (index.blade.php)
        └── dashboard.blade.php