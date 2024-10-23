## Part 3:

SalesCo is thrilled with the latest updates to the sales report! The calculations are correct and the executive team can actually read the report! They've come back with a few ideas for additional features that will make the report even more usable.
- The SalesCo executive team thinks that it would be fantastic if they could do some filtering of the data when the report is generated. They want to be able to filter the report on the Seller, that way they can provide the sales staff with a copy of the report without including data from other sales staff.
	- The input for the report generator will now have an additional parameter called "filter"
	- The filter input will filter the output of the report by either matching a sellers ID or their name
- The SalesCo executive team thinks that sorting the data in their spreadsheet software is too much work, they're rather the data come out of the report generator pre-sorted. They're willing to provide input to the report generator on how they would like the data to be sorted.
	- The input for the report generator will now have two additional parameters, "sortBy" and "sortDirection"
	- The "sortBy" parameter will be a name of any of the fields in the report output.
	- The "sortDirection" parameter will be with "asc" for ascending order or "desc" for descending order.
