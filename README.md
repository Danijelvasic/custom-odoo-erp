## Odoo ERP Extension: Custom Addons

This repository hosts a collection of custom Odoo modules designed to extend and enhance the core functionalities of Odoo ERP. These modules introduce specific business logic improvements and additional validation rules, streamlining user workflows and ensuring compliance with business and legal requirements. The customizations focus on invoicing, financial risk management, user permissions, stock management, GDPR compliance, and eCommerce features.

### Features Implemented

1. Enhanced User Permissions for Financial Modules

* Module: `account_cancel_permission`
  Introduces permission-based visibility for canceling invoices, payments, and bank statements. Only users with the Cancel Journal Entries permission can access the cancel button, adding an extra layer of control and security.
* Technology: Custom access controls implemented using Odoo’s security model and permission groups.

2. Invoice Filtering Based on Financial Risk

* Module: `account_invoice_financial_risk_filter`
  Adds the ability to filter customer invoices based on the policy field related to financial risk. This feature enhances credit risk management by allowing users to easily identify high-risk customers.
* Technology: Uses Odoo’s advanced filtering mechanisms and customized domain logic.

3. Mandatory Invoice and Payment Fields

* Modules:
`account_invoice_payment_partner_required`
`account_payment_partner_required`
`account_vendor_reference_required`
  Ensures critical fields such as Payment Mode, Payment Terms, and Vendor Reference are mandatory during invoice creation. This helps prevent incomplete or incorrect data entry.
* Technology: Built using Odoo’s form validation framework and field constraints.

4. Company VAT Display in External Reports

* Module: brand_external_report_layout_vat
  Enhances the external report layout by displaying the company's VAT number on invoices and sales orders, ensuring compliance with tax regulations.
* Technology: Custom report templates created using QWeb, Odoo’s templating engine.

5. Hiding Sensitive Financial Information

* Module: `hide_cost_margin`
  Restricts visibility of cost and margin information to authorized users only. This feature ensures sensitive financial data is protected from unauthorized access.
* Technology: Implemented through Odoo’s access control lists (ACLs) and conditional field visibility.

6. GDPR Compliance

* Module: `l10n_es_gdpr_notification`
  Adds a GDPR compliance notification to documents, ensuring businesses meet European data protection standards.
* Technology: Implemented through Odoo’s document generation and notification features.

7. Extended Customer and Partner Management

* Module: `partner_tag_append_model`
  Adds a partner tag field to invoices and sale orders, enabling enhanced categorization and filtering of customers and partners.
* Technology: Customized form views and partner model extension using Odoo’s ORM framework.

8. Enhanced Stock and Inventory Management

* Modules:
`stock_analysis_valuation`
`stock_change_qty_reason_report`
`stock_change_qty_reason_required`
  Provides additional functionality for stock analysis by displaying current unit cost and inventory valuation. It also introduces mandatory stock change reasons, ensuring accurate inventory adjustments.
* Technology: Customized stock reports and validation rules using Odoo’s stock module.

9. VAT Validation for Invoices

* Module: `vat_checker`
  Automatically checks if a customer has a valid VAT number before creating an invoice, reducing errors and ensuring tax compliance.
* Technology: Integrated with Odoo’s VAT validation API.

10. Enhanced eCommerce Functionality

* Modules:
`website_header_searchbar`
`website_sale_brand`
  Introduces a global search bar for eCommerce sites and extends the website sale order module to support brand-specific filters, improving the user experience and product searchability.
* Technology: Built using Odoo’s website and eCommerce frameworks with custom frontend and backend components.
