Product Requirements Document (PRD)

## Purpose of this Product Requirements Document (PRD)

The purpose of this PRD is to outline the requirements for a startup growth calculator website. It will allow users to enter numeric values and see real-time calculations that represent startup growth metrics over time.

## Objectives
* Enable founders to enter values representing current growth metrics and see how they will grow over time
* Provide instant feedback so founders can change values quickly and see updated results
* Require no setup or installation (should run directly in ChatGPT or on a hosted website)

## Functional requirements

### Inputs

All inputs, unless otherwise specified, represent monthly values.

| Field                               | Abbreviation    |Type        | Min        | Max        |
| ----------------------------------- | --------------- | ---------- | ---------: | ---------: |
| Customers                           |                 | Integer    | 10         |            |
| Customers growth rate               |                 | Percent    | -100       |            |
| Customers churn rate                |                 | Percent    | -100       |            |
| Average Revenue per User            | ARPU            | Currency   | 0          |            |
| Net Retention Revenue               | NRR             | Percent    | -10        |            |
| Customer Acquisition Cost           | CAC             | Currency   | 0          |            |
| Monthly Recurring Revenue Goal      | MRR             | Currency   | 0          |            |

* Max values should be higher than minumum values
* If the column is empty then there's no constraint
* Only numeric values (included decimals) are allowed (i.e. no currency symbols, no percentage symbols)
* Percentages are entered as decimals (e.g. .05) instead of percentages (105%)


### Calculations

| Metric                              | Formula                                                                | Notes
| ----------------------------------- | ---------------------------------------------------------------------- | ----------------------------------- |
| Customers net growth rate           | Customers growth rate - customers churn rate                           |                                     |
| MRR                                 | ARPU * Customers                                                       |                                     |
| CAC payback                         | CAC / ARPU                                                             |                                     |
| Lifetime                            | 


### Outputs

* Change in real-time 

