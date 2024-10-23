## Part 1:

Welcome to Real Software LLC! We're excited to have you as part of our team! We got a lot of totally real clients that need software to do things for them, so let's get you started with one of our latest clients.

SalesCo International is client that we signed a contract with right before you started. They're a company based… somewhere. All we've gotten from them is that the weather is nice year-round, they often work from the beach, and the tax situation is good for them. They got a lot of sales staff that are selling a lot of whatever it is that SalesCo sells to a lot of buyers. All good news for SalesCo! Unfortunately their sales records are plentiful and the executives are unhappy with having to summarize the data themselves. That's where we (or more specifically, you) come in! We've been contracted to build a reporting system for SalesCo.

SalesCo has provided some example data from their current sales records system which comes in json files:

```
[
	{
		"Id": "c62612a3-f8f8-4a16-bbe5-c7ff89a954f5",
		"Date": "1970-01-01T00:00:00.000Z",
		"Price": 157.50,
		"Count": 38,
		"Item": {
			"Id": "4021740f-02b4-4bb7-a599-ad1ee9045bfd",
			"Name": "Computer parts, misc"
			"Cost": 150.99
		},
		"Seller": {
			"Id": "8f9dd7d9-2bac-45cf-8fd3-70d77aba7ef4",
			"Name": "Robert Smith"
		},
		"Buyer": {
			"Id": "91c900ba-4ca5-4a00-b39c-c9c9285c641b",
			"Name": "Cyber Dynamics, LLC"
		}
	},
	{
		"Id": "024f6a96-c326-4964-ab45-3f2c185ecda2",
		"Date": "1997-08-29T02:14:00.000-04",
		"Price": 96.16,
		"Count": 70,
		"Item": {
			"Id": "7a2c7027-9a4b-424f-b5c7-dd78e4aa7375",
			"Name": "T-800 CSM-101"
			"Cost": 87.42
		},
		"Seller": {
			"Id": "8f9dd7d9-2bac-45cf-8fd3-70d77aba7ef4",
			"Name": "Bob Smith"
		},
		"Buyer": {
			"Id": "91c900ba-4ca5-4a00-b39c-c9c9285c641b",
			"Name": "Cyberdyne Systems"
		}
	},
	{
		"Id": "0252ff9c-71ea-49d1-8584-50093789bd50",
		"Date": "2000-01-01T00:00:00.000Z",
		"Price": 22.28,
		"Count": 81,
		"Item": {
			"Id": "333cd6d6-987b-440f-94e1-17ea3eb51591",
			"Name": "Computer clock"
			"Cost": 19.37
		},
		"Seller": {
			"Id": "8f9dd7d9-2bac-45cf-8fd3-70d77aba7ef4",
			"Name": "Bob Smith"
		},
		"Buyer": {
			"Id": "196db142-d572-48e0-980a-e5939eafd63c",
			"Name": "Alice Supply Co"
		}
	},
	{
		"Id": "0252ff9c-71ea-49d1-8584-50093789bd50",
		"Date": "2012-12-21T12:21:00.000Z",
		"Price": 306.88,
		"Count": 74,
		"Item": {
			"Id": "a3c13259-d3fa-4cc3-bccb-ab97bbd211f7",
			"Name": "Paper calendar"
			"Cost": 255.73
		},
		"Seller": {
			"Id": "8f9dd7d9-2bac-45cf-8fd3-70d77aba7ef4",
			"Name": "SMITH, ROBERT"
		},
		"Buyer": {
			"Id": "196db142-d572-48e0-980a-e5939eafd63c",
			"Name": "Alice Supply Co"
		}
	},
	...
]
```

SalesCo leadership is looking to get the data summarized by Seller and Buyer. They don’t care to know about the exact items that were sold, just how much is being sold to each buyer by each sales staff member.

### Acceptance Criteria:

- SalesCo expects the report to be in a json file
- The report should have the following fields
	-   Seller
	-   Buyer
	-   Sales
	-   Count
- The Sales field should be calculated with the following formula:
	- Sales = Item Cost * Sale Count
- The Count field should be the number of unique sales for the seller/buyer grouping

### Hints:

- Start with summarizing data for a single sales person/buyer combo, then re-use the code generate a record for each sales person/buyer combo
- Don't focus too much on the json parsing/serialization, use what's built into your programming language (or assume a third party library can do it for you)
- Pay attention to the input data, there could be some weirdness
	- Names change over time, IDs are forever. What should you use as the seller/buyer in the output?
	