# HomeLander


INSERT INTO catalog (
    catalog_id, catalog_name, start_date, end_date, is_active, 
    created_date, update_date, catalog_description
) VALUES
(1, 'Summer Collection 2023', '2023-06-01', '2023-08-31', 1, '2023-05-15', '2023-05-18', 'Featured summer apparel and accessories.'),
(2, 'Winter Essentials 2023', '2023-11-01', '2024-01-31', 0, '2023-10-20', '2023-10-25', 'Cozy winter wear and holiday-themed products.'),
(3, 'Spring Sale 2024', '2024-03-15', '2024-05-31', 1, '2024-02-10', '2024-02-12', 'Discounted spring fashion and seasonal decor.'),
(4, 'Back-to-School 2023', '2023-08-01', '2023-09-15', 0, '2023-07-20', '2023-07-25', 'School supplies and trendy student gear.'),
(5, 'Holiday Special 2023', '2023-11-20', '2023-12-31', 1, '2023-11-01', '2023-11-05', 'Limited-edition gifts and festive decorations.'),
(6, 'Autumn Fashion 2023', '2023-09-01', '2023-11-15', 0, '2023-08-20', '2023-08-25', 'Warm sweaters and boots for fall.'),
(7, 'Summer Clearance 2023', '2023-09-01', '2023-09-30', 0, '2023-08-15', '2023-08-20', 'Discounted summer items for quick sale.'),
(8, 'New Year 2024', '2024-01-01', '2024-01-31', 1, '2023-12-15', '2023-12-20', 'Resolutions-themed products and fitness gear.'),
(9, 'Valentine\'s Day 2024', '2024-02-01', '2024-02-29', 1, '2024-01-10', '2024-01-15', 'Romantic gifts and couples\' accessories.'),
(10, 'Spring Break 2024', '2024-03-10', '2024-04-10', 1, '2024-02-20', '2024-02-25', 'Travel-friendly apparel and beach essentials.'),
(11, 'Memorial Day 2024', '2024-05-25', '2024-06-01', 1, '2024-05-10', '2024-05-15', 'Patriotic-themed apparel and home decor.'),
(12, 'Summer BBQ Collection', '2024-06-01', '2024-08-31', 1, '2024-05-15', '2024-05-20', 'Outdoor grilling tools and summer party supplies.'),
(13, 'Fall Harvest 2024', '2024-09-01', '2024-11-15', 1, '2024-08-20', '2024-08-25', 'Autumn-themed home goods and seasonal snacks.'),
(14, 'Black Friday 2024', '2024-11-29', '2024-12-02', 1, '2024-11-15', '2024-11-20', 'Massive discounts on electronics and fashion.'),
(15, 'Year-End Clearance 2024', '2024-12-15', '2024-12-31', 1, '2024-12-01', '2024-12-05', 'Final sale on remaining inventory.');




-- Insert sample data (15 rows, with 1-3 categories per catalog)
INSERT INTO catalog_category (
    catalog_id, category_id, priority, created_date
) VALUES
-- Summer Collection 2023 (Catalog 1)
(1, 1, 1, '2023-05-18'),  -- Apparel
(1, 2, 2, '2023-05-18'),  -- Accessories

-- Winter Essentials 2023 (Catalog 2)
(2, 1, 1, '2023-10-25'),  -- Apparel

-- Spring Sale 2024 (Catalog 3)
(3, 1, 1, '2024-02-12'),  -- Apparel
(3, 3, 2, '2024-02-12'),  -- Home Decor

-- Back-to-School 2023 (Catalog 4)
(4, 1, 1, '2023-07-25'),  -- Apparel
(4, 4, 2, '2023-07-25'),  -- School Supplies

-- Holiday Special 2023 (Catalog 5)
(5, 5, 1, '2023-11-05'),  -- Gifts
(5, 3, 2, '2023-11-05'),  -- Home Decor

-- Autumn Fashion 2023 (Catalog 6)
(6, 1, 1, '2023-08-25'),  -- Apparel

-- Summer Clearance 2023 (Catalog 7)
(7, 1, 1, '2023-08-20'),  -- Apparel

-- New Year 2024 (Catalog 8)
(8, 5, 1, '2023-12-20'),  -- Gifts
(8, 4, 2, '2023-12-20'),  -- Fitness Gear

-- Valentine's Day 2024 (Catalog 9)
(9, 5, 1, '2024-01-15'),  -- Gifts
(9, 2, 2, '2024-01-15'),  -- Accessories

-- Spring Break 2024 (Catalog 10)
(10, 1, 1, '2024-02-25'), -- Apparel
(10, 6, 2, '2024-02-25'), -- Travel Gear

-- Memorial Day 2024 (Catalog 11)
(11, 7, 1, '2024-05-15'), -- Patriotic Items

-- Summer BBQ Collection (Catalog 12)
(12, 8, 1, '2024-05-20'), -- Grilling Tools
(12, 9, 2, '2024-05-20'), -- Party Supplies

-- Fall Harvest 2024 (Catalog 13)
(13, 3, 1, '2024-08-25'), -- Home Decor
(13, 10, 2, '2024-08-25'),-- Seasonal Snacks

-- Black Friday 2024 (Catalog 14)
(14, 4, 1, '2024-11-20'), -- Electronics
(14, 1, 2, '2024-11-20'), -- Apparel

-- Year-End Clearance 2024 (Catalog 15)
(15, 1, 1, '2024-12-05'), -- Apparel
(15, 5, 2, '2024-12-05'); -- Gifts

INSERT INTO category (category_id, category_name, created_date) VALUES
(1, 'Apparel', '2022-01-15'),
(2, 'Accessories', '2022-02-01'),
(3, 'Home Decor', '2022-03-10'),
(4, 'School Supplies', '2022-04-05'),
(5, 'Gifts', '2022-05-20'),
(6, 'Travel Gear', '2023-01-10'),
(7, 'Patriotic Items', '2023-02-14'),
(8, 'Grilling Tools', '2023-03-20'),
(9, 'Party Supplies', '2023-04-15'),
(10, 'Seasonal Snacks', '2024-01-10');



INSERT INTO child_category (category_id, child_category_id, created_date) VALUES
-- Apparel (1) → Accessories (2)
(1, 2, '2022-02-01'),
-- Apparel (1) → Travel Gear (6)
(1, 6, '2023-01-15'),
-- Home Decor (3) → Party Supplies (9)
(3, 9, '2023-04-20'),
-- Gifts (5) → Seasonal Snacks (10)
(5, 10, '2024-01-15'),
-- School Supplies (4) → Patriotic Items (7)
(4, 7, '2023-02-20'),
-- Grilling Tools (8) → Apparel (1) [Cross-category relationship]
(8, 1, '2023-05-01');





INSERT INTO product (product_id, product_name, created_date) VALUES
(1, 'Wireless Headphones', '2023-01-15'),
(2, 'Smart Watch', '2023-02-20'),
(3, 'Bluetooth Speaker', '2023-03-10'),
(4, 'Power Bank', '2023-04-05'),
(5, 'LED Lamp', '2023-05-20'),
(6, 'Yoga Mat', '2023-06-12'),
(7, 'Water Bottle', '2023-07-08'),
(8, 'Notebook', '2023-08-25'),
(9, 'Desk Lamp', '2023-09-18'),
(10, 'Coffee Mug', '2023-10-10'),
(11, 'Backpack','2023-11-05'),
(12, 'Umbrella', '2023-12-01'),
(13, 'Sunglasses', '2024-01-15'),
(14, 'Jacket', '2024-02-20'),
(15, 'Sneakers', '2024-03-10'),
(16, 'Handbag', '2024-04-05'),
(17, 'Watch Strap', '2024-05-20'),
(18, 'Phone Case', '2024-06-12'),
(19, 'Laptop Stand', '2024-07-08'),
(20, 'Desk Organizer', '2024-08-25');


INSERT INTO product_category_catalog 
(product_id, category_id, catalog_id, created_date) VALUES
-- Product 1: Wireless Headphones
(1, 2, 1, '2023-05-18'),  -- Accessories → Summer Collection 2023
(1, 2, NULL, '2023-01-15'), -- General Accessories (no catalog)

-- Product 2: Smart Watch
(2, 2, 5, '2023-11-05'),  -- Accessories → Holiday Special 2023
(2, 4, NULL, '2023-02-20'), -- School Supplies (general)

-- Product 3: Bluetooth Speaker
(3, 8, 12, '2024-05-20'), -- Grilling Tools → Summer BBQ Collection
(3, 9, NULL, '2023-03-10'), -- Party Supplies (general)

-- Product 4: Power Bank
(4, 4, 14, '2024-11-20'), -- Electronics → Black Friday 2024
(4, 1, NULL, '2023-04-05'), -- Apparel (general)

-- Product 5: LED Lamp
(5, 3, 13, '2024-08-25'), -- Home Decor → Fall Harvest 2024
(5, 7, NULL, '2023-05-20'), -- Patriotic Items (general)

-- Product 6: Yoga Mat
(6, 1, 3, '2024-02-12'),  -- Apparel → Spring Sale 2024
(6, 10, NULL, '2023-06-12'),-- Seasonal Snacks (general)

-- Product 7: Water Bottle
(7, 1, 10, '2024-02-25'), -- Apparel → Spring Break 2024
(7, 6, NULL, '2023-07-08'), -- Travel Gear (general)

-- Product 8: Notebook
(8, 4, 4, '2023-07-25'),  -- School Supplies → Back-to-School 2023
(8, 5, NULL, '2023-08-25'), -- Gifts (general)

-- Product 9: Desk Lamp
(9, 3, 13, '2024-08-25'), -- Home Decor → Fall Harvest 2024
(9, 3, NULL, '2023-09-18'), -- Home Decor (general)

-- Product 10: Coffee Mug
(10, 5, 5, '2023-11-05'), -- Gifts → Holiday Special 2023
(10, 10, NULL, '2023-10-10'); -- Seasonal Snacks (general)




INSERT INTO sku 
(sku_name, Sku_description, price, quantity, product_id, created_date) VALUES
-- Product 1: Wireless Headphones
('WH-BLUE', 'Blue Bluetooth Headphones', 49.99, 150, 1, '2023-05-18'),
('WH-BLACK', 'Black Bluetooth Headphones', 49.99, 120, 1, '2023-05-18'),

-- Product 2: Smart Watch
('SW-SILVER', 'Silver Stainless Steel Watch', 99.99, 80, 2, '2023-02-20'),
('SW-GOLD', 'Gold-Plated Watch', 129.99, 50, 2, '2023-02-20'),

-- Product 3: Bluetooth Speaker
('BS-PORTABLE', 'Portable Waterproof Speaker', 29.99, 200, 3, '2023-03-10'),
('BS-HOME', 'Home Theater Speaker', 79.99, 60, 3, '2023-03-10'),

-- Product 4: Power Bank
('PB-10K', '10,000mAh Power Bank', 19.99, 300, 4, '2023-04-05'),
('PB-20K', '20,000mAh Power Bank', 29.99, 180, 4, '2023-04-05'),

-- Product 5: LED Lamp
('LED-DESK', 'Desk LED Lamp', 14.99, 250, 5, '2023-05-20'),
('LED-NIGHT', 'Night Light LED Lamp', 9.99, 400, 5, '2023-05-20'),

-- Product 6: Yoga Mat
('YM-NONSLIP', 'Non-Slip Yoga Mat', 19.99, 100, 6, '2023-06-12'),
('YM-TRAVEL', 'Foldable Travel Yoga Mat', 24.99, 70, 6, '2023-06-12'),

-- Product 7: Water Bottle
('WB-500ML', '500ml Stainless Steel Bottle', 12.99, 350, 7, '2023-07-08'),
('WB-1L', '1L Insulated Water Bottle', 19.99, 200, 7, '2023-07-08'),

-- Product 8: Notebook
('NB-A5', 'A5 Size Notebook', 4.99, 500, 8, '2023-08-25'),
('NB-LARGE', 'Large Ruled Notebook', 7.99, 300, 8, '2023-08-25'),

-- Product 9: Desk Lamp
('DL-CLAMP', 'Clamp Desk Lamp', 24.99, 90, 9, '2023-09-18'),
('DL-TASK', 'Task Lighting Desk Lamp', 34.99, 60, 9, '2023-09-18'),

-- Product 10: Coffee Mug
('CM-CERAMIC', 'Ceramic Coffee Mug', 8.99, 400, 10, '2023-10-10'),
('CM-INSULATED', 'Insulated Travel Mug', 12.99, 250, 10, '2023-10-10');




CREATE TABLE sku_feature (
    sku_id INT NOT NULL,
    attribute VARCHAR(50) NOT NULL,
    value VARCHAR(255) NOT NULL,
    created_date DATE NOT NULL,
    PRIMARY KEY (sku_id, attribute),
    FOREIGN KEY (sku_id) REFERENCES sku(sku_id) ON DELETE CASCADE
);

INSERT INTO sku_feature (sku_id, attribute, value, created_date) VALUES
-- Wireless Headphones (SKU 1-2)
(1, 'Color', 'Blue', '2023-05-18'),
(1, 'Battery Life', '20 hours', '2023-05-18'),
(2, 'Color', 'Black', '2023-05-18'),
(2, 'Battery Life', '20 hours', '2023-05-18'),

-- Smart Watch (SKU 3-4)
(3, 'Display Type', 'Touchscreen', '2023-02-20'),
(3, 'Water Resistance', '50m', '2023-02-20'),
(4, 'Display Type', 'Touchscreen', '2023-02-20'),
(4, 'Band Material', 'Stainless Steel', '2023-02-20'),

-- Bluetooth Speaker (SKU 5-6)
(5, 'Waterproof Rating', 'IPX7', '2023-03-10'),
(5, 'Power Source', 'Battery', '2023-03-10'),
(6, 'Waterproof Rating', 'IPX5', '2023-03-10'),
(6, 'Power Source', 'USB', '2023-03-10'),

-- Power Bank (SKU 7-8)
(7, 'Capacity', '10,000mAh', '2023-04-05'),
(7, 'Output Ports', 'USB-A', '2023-04-05'),
(8, 'Capacity', '20,000mAh', '2023-04-05'),
(8, 'Output Ports', 'USB-C', '2023-04-05'),

-- LED Lamp (SKU 9-10)
(9, 'Color Temperature', 'Cool White', '2023-05-20'),
(9, 'Brightness Levels', '3', '2023-05-20'),
(10, 'Color Temperature', 'Warm White', '2023-05-20'),
(10, 'Dimmable', 'Yes', '2023-05-20'),

-- Yoga Mat (SKU 11-12)
(11, 'Material', 'PVC', '2023-06-12'),
(11, 'Thickness', '5mm', '2023-06-12'),
(12, 'Material', 'Rubber', '2023-06-12'),
(12, 'Foldable', 'Yes', '2023-06-12'),

-- Water Bottle (SKU 13-14)
(13, 'Capacity', '500ml', '2023-07-08'),
(13, 'Material', 'Stainless Steel', '2023-07-08'),
(14, 'Capacity', '1000ml', '2023-07-08'),
(14, 'Insulated', 'Yes', '2023-07-08'),

-- Notebook (SKU 15-16)
(15, 'Size', 'A5', '2023-08-25'),
(15, 'Pages', '100', '2023-08-25'),
(16, 'Size', 'A4', '2023-08-25'),
(16, 'Paper Type', 'Ruled', '2023-08-25'),

-- Desk Lamp (SKU 17-18)
(17, 'Adjustable Head', 'Yes', '2023-09-18'),
(17, 'Brightness Levels', '5', '2023-09-18'),
(18, 'Adjustable Head', 'Yes', '2023-09-18'),
(18, 'Color', 'Silver', '2023-09-18'),

-- Coffee Mug (SKU 19-20)
(19, 'Material', 'Ceramic', '2023-10-10'),
(19, 'Capacity', '350ml', '2023-10-10'),
(20, 'Material', 'Stainless Steel', '2023-10-10'),
(20, 'Insulated', 'Yes', '2023-10-10');
