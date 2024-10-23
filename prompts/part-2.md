## Part 2:

SalesCo was thrilled to get the report software we delivered to them! We're definitely making it easier for them to sell… whatever it is they're selling. However after using the sales software for a little bit, they found some issue's they'd like get fixed.

- The Sales field calculation was incorrect. Apparently our contact at SalesCo got some bad information about the calculation, the corrected calculation should be:
	- Sales = Sale Price * Sale Count
- The Count field calculation was incorrect. Instead of getting the number of unique sales, the executives are more interested in know exactly how many items were sold. We should instead sum up the Sale Count field for the Count column.
- The executives are looking to optimize their costs and want to know exactly how much they're paying on taxes for their sales. We need to add a Taxes field to the report. The Taxes field should be calculated using the following formula:
	- Taxes = ( Sale Price - Item Cost ) * Sale Count
- The SalesCo executive team has been having issues loading the report into their favorite spreadsheet software. Turns out half of the executives haven't even heard of a json file before. They'd much rather have the report be in a csv file instead.

### Hints:

- When making a csv file, don't forget to include a header row
- When writing data to the csv file, be aware if the columns you're writing have commas in them
