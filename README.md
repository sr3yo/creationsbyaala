
---

# CreationsByAala

CreationsByAala is a full-stack PHP web application built for a local bakery, "CreationsByAala". It lets customers browse products by category, add items to a cart, place orders, and view receipts. The app demonstrates a complete small-business e-commerce workflow and can be adapted for other stores.

Customers can browse items organized into categories like cakes and pastries, add products to a cart, and update quantities before checkout. Orders can be placed, and receipts are generated for each purchase. User authentication allows customers to log in and view their order history. Session management is implemented using PHP sessions to maintain cart state and user login status. Form submissions are validated both client-side (JavaScript) and server-side (PHP) to ensure data integrity.

The project is built with PHP for backend logic, HTML, CSS, and JavaScript for the front-end interface, and can connect to a MySQL database through `connect.php` if needed. The cart system uses JavaScript for dynamic updates, while PHP handles server-side data persistence and order processing. Product data can be stored either in PHP arrays or a MySQL database, and prepared statements are used for database interactions to prevent SQL injection. The application follows a modular file structure, separating concerns such as login, cart, purchase, and receipt handling into individual folders for maintainability.

To set up the project locally:

1. Clone the repository:

   ```bash
   git clone https://github.com/sr3yo/creationsbyaala.git
   cd creationsbyaala
   ```
2. Install a local web server such as XAMPP, MAMP, or WAMP.
3. Place the project folder in the web server’s root directory (for example, `htdocs` in XAMPP).
4. Start the web server (and MySQL if using a database).
5. If using a database, create one and update the credentials in `connect.php`. For example:

   ```php
   <?php
   $conn = new mysqli("localhost", "username", "password", "creationsbyaala");
   if ($conn->connect_error) {
       die("Connection failed: " . $conn->connect_error);
   }
   ?>
   ```
6. Open the project in a browser at `http://localhost/creationsbyaala/`.

The application can be customized by updating product listings, modifying styles, replacing images and logos, or adding an admin panel for inventory management. Contributions are welcome—fork the repository, make improvements, and submit a pull request. The project currently has no license, so contact the owner before any commercial use.
