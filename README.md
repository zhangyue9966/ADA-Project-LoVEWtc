# ADA Project: Fraud Detection

Reference: https://www.kaggle.com/c/ieee-fraud-detection/overview

**Group: 19**

Previous Meeting Time: 10/20/2019(Sun); 10/23/2019(Wed)

**Next Meeting Time: TBD**


## 1: Data Processing
### 1.1: Imbalanced Data
Starting points:
- Dsampling(trival)
- Upsampling(trival)
- SMOTE
### 1.2: Missing Value
Starting points:
- Delete
- Median,Mod,Mean
- Regression
- Multiple imputation
- Maximum Likelihood: 
  - Direct Maximum Likelihood
  - The Expectation-maximization (EM) algorithm
- Bayesian simulation methods
  - Schafer algorithms
  - Van Buuren algorithm
- Hot deck imputation methods
- more advanced regression technics

## 2: Feature Selection
Starting points:
- Filter Method(Fisher Criteria
- Wrapped Method
  - Forward Stepwise selection
  - Backward Stepwise selection
- Embedded Method(Lasson)

## 3: Modeling Fitting
Starting points: 
- Logistic
- SVM
- LGBM(refer to Kaggle NB)

## [Data Description](https://www.kaggle.com/c/ieee-fraud-detection/discussion/101203)

### Transaction Table

**TransactionDT:** timedelta from a given reference datetime (not an actual timestamp)

**TransactionAMT:** transaction payment amount in USD

**ProductCD:** product code, the product for each transaction

**card1 - card6:** payment card information, such as card type, card category, issue bank, country, etc.
addr: address

**dist:** distance

**P_ and (R__) emaildomain:** purchaser and recipient email domain

**C1-C14:** counting, such as how many addresses are found to be associated with the payment card, etc. The actual meaning is masked.

**D1-D15:** timedelta, such as days between previous transaction, etc.

**M1-M9:** match, such as names on card and address, etc.

**Vxxx:** Vesta engineered rich features, including ranking, counting, and other entity relations.

### Categorical Features:

**ProductCD**

**card1 - card6**

**addr1, addr2**

**Pemaildomain Remaildomain**

**M1 - M9**

### Identity Table

Variables in this table are identity information – network connection information (IP, ISP, Proxy, etc) and digital signature (UA/browser/os/version, etc) associated with transactions.

They're collected by Vesta’s fraud protection system and digital security partners.

(The field names are masked and pairwise dictionary will not be provided for privacy protection and contract agreement)

### Categorical Features:

**DeviceType**

**DeviceInfo**

**id12 - id38**

