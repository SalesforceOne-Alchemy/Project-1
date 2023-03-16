# Entities to Objects

## Business Needs brief (pull entities from below)

United Solar, as mentioned earlier, is a solar panel production and installation company. Their solar panel products are sold to both businesses and households and the sales representatives need to often get in contact with these places. Sometimes, our sales reps get some lead on a potential sale and they like to have that distinguished from the businesses that United Solar has already sold to. Businesses are often repeat customers, and our sales reps also like to have those upcoming deals tracked. Businesses can often pay the entire installation amount up front, but often times households need to pay in installations using payment receipts. In case of issues with the products, United Solar also would like a ticketing system set up. The installation of certain solar panels requires a certification, or multiple. United Solar wants to keep track of the certifications a solar panel needs for installation and which engineers hold that certification. When an installation is requested, it's tracked through a work order. Finally, internal employees, especially engineers, need to be able to make reimbursment requests for expenses when they're on installation.

### Account (Standard)

- Business
- Household


#### Fields

- Name : text
- Account ID : unique auto-number
- Type: Picklist
  - Business
  - Household
- [FK] Primary Contact -> Contact ID

### Contact (Standard)

- Sales Representative
- Engineer

#### Fields
- [PK] Contact ID : unique auto-number
- First Name : text
- Last Name : text
- Salutation : Picklist
- Phone Number : Number

### Lead (Standard)

#### Fields

- [PK] Lead ID: unique auto-number
- [FK] Opportunity -> Opportunity ID

### Campaign (Standard)

### Opportunity (Standard)

#### Fields

- [PK] Opportunity ID : unique auto-number
- [FK] Account -> Account ID

### Installation (Custom)

#### Fields

- [PK] Installation ID : unique auto-number
- Date & Time Started : DateTime
- Date & Time Ended : DateTime
- [FK] Account -> Account ID

### Product (Custom)

#### Fields
- [PK] Product ID : unique auto-number
- Product Name : Text
- Cost per unit : Currency
- Units in Stock : Number

### Case (Standard)

- Issues 

#### Fields

- [PK] Case Number : unique auto-number
- [FK] Account -> Account ID
- [FK] Primary Contact/Case Issuer -> Contact ID

### Certification (Custom)

#### Fields
### Work Order (Custom)

### Reimbursment (Custom)
