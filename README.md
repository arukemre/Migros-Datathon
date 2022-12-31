<img src= "[https://www.wvnstv.com/wp-content/uploads/sites/76/2022/02/Outage-file-image.jpg](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.aa.com.tr%2Ftr%2Fsirkethaberleri%2Fperakende%2Fmigros-money-gold-uyelerine-ozel-firsat-ve-hizmetler-sunuluyor%2F665584&psig=AOvVaw2mLevHx8kKbhzmzkk_D5aE&ust=1672588638831000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNjBj7CcpPwCFQAAAAAdAAAAABAE)" alt ="Titanic" style='width: 15000;'>

# Migros DATATHON
## Project descriptions 

Hi everyone.I want to briefly introduce this competition and the organizer of the competition. This competition was created on the Kaggle platform and 284 competitors joined it. Competition is a classification problem and the organization owner demands the best f1 score. Migros a.ş the organizer of the competition, One of the biggest retail and e-commerce companies in the Turkey market intended the best customer experience for customers. Migros want to forecast which customer will back return to offers, thus  Migros can send new offers to these customers .To ensure sustainable customer and achieve new customers for the Company that main target.
for this purpose, Migros want to a model that getting the best-predicted result taking into account the f1 score


```
Migros-datathon/
├─ data/
|─ migros-datathon-2022.ipynb/
  
  |─Data Preview
  |─Data preprocessing
  |─Data preprocessing  and Feature Engineering stages
  |─ XGBOOST MODEL
  |─ Model optimization with optuna
```

## Dataset Descriptions

* train.csv - Training dataset
* test.csv - Test dataset
* transaction_header.csv – Receipt information
* transaction_sale.csv – Information of products in receipts
* product_groups.csv – Category breakdowns with campaign categories
* customeraccount.csv – cardnumber-individualnumber match
* customer.csv – Customer demographics
* general_categories.csv – General category names.


`Train/Test`
* individualnumber: Customer's contact number
* category_number: Campaign category from which the campaign was launched.
* hakkedis_amt: The minimum amount of expenditure (TL) that must be made in the specified category in order to benefit from the campaign.
* odul_amt: The amount of reward points to be obtained when using the campaign
* response: Customer benefit from the campaign (1: Benefited, 0: Not Benefited) LABEL COLUMN

`Transaction Header`
* date_of_transaction: Receipt date
* basketid: Token number
* cardnumber: The card number used for shopping (matches the cardnumber in the customeraccount table)
* is_sanal: The virtuality of the shopping to which the voucher corresponds (1: Virtual Shopping, 0: Shop Shopping)

`Transaction Sale`
* basketid: The number of the receipt in which the product is included
* category_level_1: Category 1 Level (Top level of category hierarchy)
* category_level_2: Level 2 Category
* category_level_3: 3rd Level Category
* category_level_4: 4th Level Category (lowest level of category hierarchy)
* amount: Product amount
* quantity: The number of products in products sold as a unit, the weight of the product in products sold by weighing
* discount_type_1: Percentage of type 1 discount
* discount_type_2: Percentage of the second type of discount
* discount_type_3: Percentage of type three discount

`Product Groups`
* category_number: The category used in the campaigns.
* category_level_1: Category 1 Level (Top level of category hierarchy)
* category_level_2: Level 2 Category
* category_level_3: 3rd Level Category
* category_level_4: 4th Level Category (lowest level of category hierarchy)

`Customer Account`
* individualnumber: Matches the individualnumber in the Promotion train/test table.
* cardnumber: Matches the customer_number in the transaction header table.

`customers`
* individualnumber
* gender: The gender of the customer
* city code: Customer's city code
* dateofbirth: Customer's birth year
