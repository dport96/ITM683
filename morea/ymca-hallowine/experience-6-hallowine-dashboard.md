---
title: "Hallowine Dashboard Project"
published: true  
morea_id: experience-ymca-dashboard-project 
morea_type: experience  
morea_summary: "Create a dashboard showcasing all of the data analyzed from previous experiences"
morea_sort_order: 5  
morea_labels: Dashboard Project
---  
# Hallowine Dashboard Project
## Table of Contents
- [Hallowine Dashboard Project](#hallowine-dashboard-project)
  - [Table of Contents](#table-of-contents)
  - [Objective](#objective)
  - [Dashboard Requirements](#dashboard-requirements)
    - [Decisions to be supported:](#decisions-to-be-supported)
    - [Quality:](#quality)
    - [Non-functional Requirements:](#non-functional-requirements)
    - [Documentation:](#documentation)
  - [Design](#design)
    - [Dashboard Components:](#dashboard-components)
    - [Interactive Ability](#interactive-ability)
  - [Project Management and Expectations](#project-management-and-expectations)
    - [Project Architect and Coordinator:](#project-architect-and-coordinator)

## Objective  
Provide an Excel-based user-interactive information dashboard to inform decision-makers in making confident auction management decisions.  

## Dashboard Requirements 
### Decisions to be supported:
- How many items to have in the auction (total and by category)
- Solicitation targets
- Accept an item or ask for a cash donation
- Auction management (min bid, increment, enforcement, etc.)

### Quality:
- High integrity: all dashboard elements are firmly grounded on data and clear analytics (no opinions)
- High utility: dashboard provides clear useful information for improving decision confidence
- High usability: dashboard is easy to utilize by non-experts without assumed statistical/analytical knowledge or expertise

### Non-functional Requirements:
- All components must be interactive and enable the user to explore scenarios
- Informing decisions, not making decisions
- Must use only existing data (e.g. cannot use data not available)
- Must assume existing auction process and practices (e.g. cannot assume there will be real-time bidding information)
- Must be updatable to add new auction data so it can be used in subsequent auctions

### Documentation:
- Each component must provide a detailed description of the models used, how they were developed, and how they are used in decision-making.
- Users guide with examples on using the dashboard to make decisions

## Design
### Dashboard Components:
Keep interactive ability in mind. These are metrics that will be shown to the user after they select an item's information or goal.  

1. Performance analysis of the previous auction:
   - Number of items, total sales, percent sold, percent undersold, opportunity loss, etc. by aggregate or category, top-bottom categories for various variables (sales, value, sold, opportunity loss, etc.)
   - Anomaly detection, include visual indicators of outliers

2. Optimal numbers of items by category based on demand predictions and cost objectives:
   - Allows users to adjust overage and underage costs and perform best guess demand
   - Allows users to choose different optimality goals such as minimizing expected loss, maximizing sales, selling at least X% of the items, etc.  

3. Solicitation categories priorities assessment:
   - Allows users to prioritize between all given solicitation categories  

4. Donated item risk assessment:
   - Allows users to input an item value, category, size, description etc. and see the associated risks (opportunity loss, sale likelihood, etc.) and benefits (expected sale amount, expected interest, etc.) based on historical data, predictive model outputs, current inventory of items in auction, and goal priorities (e.g. maximize sales, minimize opportunity loss, etc.). This could include visual indicators of potential performance, such as traffic light colors (green for low risk, yellow for medium, red for high risk).

5. Minimum bid and increment suggestion:
   - Allows users to input an item value, category, size and provides suggested min bid and increment along with adjustment considerations. Users can adjust by goal priority e.g. maximum sale price, highest interest, maximize sale likelihood, etc.
   - What would be good ways to set the min. bid and increment that would give them use of it
   - They originally set min. bid based on value of item value, with some deviation based on category
   - Sometimes 40% of value, if its lower value– will place smaller percentage of value to set a min. bid
   - For it to be a bargain– they have to make the min. bid too low
   - Inputs should be what they are concerned about: value
   - “Perceived Bargain” vs “Sales Price”
   - We have increment optimal model in YMCA
   - Value - sales=a0 is Y
   - X is min. bid a1
   - Things they might care about: set goal like high sales price, high interest, etc., ability to sell (minimal opportunity loss)

6. Items in the auction tracker:
   - Keeps track of information for items accepted for the auction
   - Data can be used in other components of the dashboard, such as number of items in auction, number of items in a given category, etc.
   - Provides performance projections, such as sales expectations,  percentage of items that will sell, average expected interest, etc.

### Interactive Ability

For choosing whether or not to accept an item:
   - Users can select an item category for a dropdown
   - Users can select an item value range (low, medium, high)
   - Users can select an item size (1, 2, 3, 4, 5)

For deciding goals:
   - Users can select from the following optimality goals:
   - Minimizing expected loss
   - Maximizing sales
   - Selling at least X% of the items (provide an input field where users can enter their target percentage)

**Item Input Fields:** Implement dropdown menus using Excel's Data Validation feature to allow users to select an item category, value and size. Populate these dropdowns with the values from the data.
**Goal Input Fields:** Create dedicated input cells where users can type in their specific bid or donation goals. Use Excel's Data Validation feature to ensure that only numerical values are entered.
**Dropdown Selection for Goal Type:** Include a dropdown menu next to the input fields for users to specify whether the goal is related to bids or donations.

## Project Management and Expectations

### Project Architect and Coordinator:

One team for each component
   - Details and clarifies requirements
   - Designs, implements, and tests the component
   - Coordinates with architect to ensure all components work together*
   - Writes documentation for the component

*Many components will depend on each other

1. Performance analysis of the previous auction
   - Overview of how categories have performed over certain variables
   - Separate table for benchmarks

2. Optimal numbers of items by category based on demand predictions and cost objectives
   - Choose different optimality goals and see expected demand
   - Profit from maximum quantity

3. Solicitation categories priorities assessment Team
   - Calculate average minimum bids, estimated values, and sales prices within each category to understand their desirability and potential revenue impact and inform solicitation.
   - Bid Analysis
   - Success Rates
   - Risk Factors (Sold/Unsold)

4. Donated item risk assessment Team
   - Risk percentage for Item value, sales price, interest, opportunity loss

5. Minimum bid and increment suggestion Team
   - Provided adjusted values for min. bid and increments