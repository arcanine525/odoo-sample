# Things to consider:
- product
- customer
- staff 
- supplier - company
- inventory
- order

# Customer - User
A 'partner' is either a person, an association, an organization (company*). * It is better if you don't use company in this definition, as it has another meaning in Odoo.

A 'company' (the way it is more commonly used) is a set of partners (mainly customers, suppliers and employees), users (logins).

An example of a company would be Odoo S.A, Odoo USA or Odoo Asia/Pacific.

A 'customer' is a partner that purchases products from a company.

An 'employee' is a partner that works for a company.

A 'supplier' is a partner that sells products to a company.

Odoo is implemented by people who work for Companies. People are modelled as partners, as are the individuals and organizations that those people buy from, sell to, employ and do business with.


# Product
1: product.template (Products Menu)

    Actually it is not a product it is Product template

     whenever you are creating Product (product.template) than same will be created in also (product.product)
    it contains the main product and with list of product variant (attributes)

 2: product.product (Product Variants)

     Here there are actual products with their variants as a separate products

    When ever you are creating SO or PO than actually you are using Product variants not Products



3: Product Attributes
     To create Product Variant you need add Product Attributes to that product which will automatically Create Product Variants 

     Example:
         there is an Product Named (Moto G)
         so by default it will be in product.template and product.product
         Now, if you want to add Variant than you need to create Attribute and add to that particular
         Imagine You have created Memory as an attribute and 16 GB and 32 GB as that attribute value
         than it will be total two Product in Product Variants

     You can Create Attribute From Product Categories & Attributes --> Attributes

     You can Create Attribute Values From Product Categories & Attributes --> Attribute Values

4: Product combo

# Inventory
Create a new product. Configure the product type so that it is Stockable and not a consumable.

# Tables:
```
select * from res_users;
select * from res_groups;
select * from res_company;
select * from res_company_users_rel;
select * from res_partner;
select * from res_partner_title_id_seq;

select * from sale_order
select * from sale_order_line

select * from product_product
select * from product_template
select * from product_supplierinfo
select * from product_template
```