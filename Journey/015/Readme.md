**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# QLDB Database

## Introduction

✍️ Amazon Quantum Ledger Database (Amazon QLDB) is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log owned by a central trusted authority.

Amazon QLDB to track application data changes, and maintain a complete and verifiable history of changes over time.



## Lab Steps

1. Create a Ledger

2. Create tables and insert values
```create table PersonalInfo;
INSERT INTO PersonalInfo << 

{

    'PID' : '1',

    'FirstName' : 'Paul',

    'LastName' : 'Lewis',

    'DOB' : `1994-08-19T`,

    'GovId' : 'LEWISR261LL',

    'GovIdType' : 'Driver License',

    'Address' : '1719 University Street, Seattle, WA, 98109'

},

{

    'PID' : '2',

    'FirstName' : 'Brent',

    'LastName' : 'Logan',

    'DOB' : `1967-07-03T`,

    'GovId' : '519-01-0001',

    'GovIdType' : 'Social Security Number',

    'Address' : '43 Stockert Hollow Road, Everett, WA, 98203'

}
```

3. View the table updation history
```
INSERT INTO VehicleInfo VALUE

{

    'VIN' : 'KM8SRDHF6EU074761',

    'RegNum' : 1722,

    'State' : 'WA',

    'City' : 'Kent',

    'Manufacture' : 'Tesla',

    'Model' : 'Model S',

    'PersonID' : '1',

    'Owner' : 'Paul Lewis',

    'Year' : `2020-06-25T`

}
```

Update

```
UPDATE VehicleInfo AS v SET v.Owner = 'Brent Logan', v.PersonID = '2' WHERE v.VIN = 'KM8SRDHF6EU074761'
```

Check History 

```
SELECT * FROM history(VehicleInfo)
```

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
