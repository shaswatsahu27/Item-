# 1. Create a list of products
products = ["Laptop", "Mobile Phone", "Headphones", "Smart Watch", "Camera", "Keyboard"]

# 2. Create a tuple for a sample product
sample_product = ("Laptop", 55000, "Electronics")

# 3. Print the 2nd and last product from the list
print("2nd product:", products[1])
print("Last product:", products[-1])

# 4. Append two new products and print updated list
products.append("Mouse")
products.append("Tablet")
print("Updated products list:", products)

# Extra (optional)
# Convert tuple to list, change price, and convert back to tuple
sample_product_list = list(sample_product)
sample_product_list[1] = 52000  # updated price
sample_product = tuple(sample_product_list)

print("Updated sample product tuple:", sample_product)

# Parallel list of categories matching the products list
products = ["Laptop", "Mobile Phone", "Headphones", "Smart Watch", "Camera", "Keyboard"]
categories = ["Electronics", "Electronics", "Accessories", "Wearables", "Electronics", "Accessories"]

# 1. Create a set of categories
categories_set = set(categories)
print("Initial categories set:", categories_set)

# 2. Add a new category and show duplicates are ignored
categories_set.add("Gaming")
categories_set.add("Electronics")  # duplicate
print("Categories after adding new and duplicate:", categories_set)

# 3. Check if a category exists in the set
print("Is 'Electronics' in categories?", "Electronics" in categories_set)

# Extra (optional)
# Total number of unique categories
print("Total unique categories:", len(categories_set))

# 1. Create a dictionary of product prices
price_dict = {
    "Laptop": 55000,
    "Mobile Phone": 30000,
    "Headphones": 2000,
    "Smart Watch": 8000,
    "Camera": 25000,
    "Keyboard": 1500
}

# Add a new product with price
price_dict["Mouse"] = 700

# Update the price of an existing product
price_dict["Mobile Phone"] = 28000

# Remove a product safely (handle non-existing product)
product_to_remove = "Tablet"
if product_to_remove in price_dict:
    del price_dict[product_to_remove]
else:
    print(product_to_remove, "not found in price list")

# 3. Calculate and print average price
total_price = sum(price_dict.values())
average_price = total_price / len(price_dict)
print("Average product price:", average_price)

# Extra (optional)
# Product with maximum and minimum price
max_product = max(price_dict, key=price_dict.get)
min_product = min(price_dict, key=price_dict.get)

print("Most expensive product:", max_product, "-", price_dict[max_product])
print("Least expensive product:", min_product, "-", price_dict[min_product])

# Given data (from previous tasks)
products = ["Laptop", "Mobile Phone", "Headphones", "Smart Watch", "Camera", "Keyboard"]
categories = ["Electronics", "Electronics", "Accessories", "Wearable", "Electronics", "Accessories"]

price_dict = {
    "Laptop": 55000,
    "Mobile Phone": 28000,
    "Headphones": 2000,
    "Smart Watch": 8000,
    "Camera": 25000,
    "Keyboard": 1500
}

# 1. Create catalog list of tuples (product_name, price, category)
catalog = []

for i in range(len(products)):
    product = products[i]
    price = price_dict[product]
    category = categories[i]
    catalog.append((product, price, category))

print("Catalog:", catalog)

# 2. Create category_to_products dictionary
category_to_products = {}

for product, price, category in catalog:
    if category not in category_to_products:
        category_to_products[category] = []
    category_to_products[category].append(product)

print("Category to Products:", category_to_products)

# 3. Print products in the category with maximum number of products
max_category = None
max_count = 0

for category in category_to_products:
    count = len(category_to_products[category])
    if count > max_count:
        max_count = count
        max_category = category

print("Category with maximum products:", max_category)
print("Products in this category:", category_to_products[max_category])
