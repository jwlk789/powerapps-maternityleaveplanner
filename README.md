# powerapps-maternityleaveplanner

This Power Apps solution calculates and visualizes a personalized maternity leave schedule based on company policies, observed holidays, and federal FMLA regulations. It ensures accurate day-by-day tracking and compliance.

## Features
Generates leave schedules starting from the employee’s due date

### Includes:

2 weeks of Paid Child Care Leave

4 weeks of Paid Maternity Leave

Optional PTO and unpaid leave (user-defined)

Optional transition period (user-defined number of months)

### Adjusts for:

Company holidays, including observed dates when holidays fall on weekends

Pay period start and end dates

FMLA eligibility and tracking

Skips weekends

Ensures exact leave day counts (such as 10 weekdays for child care leave)

## Technology

Power Apps - UI development and logic building

Power Fx - Formula language for logic and behavior

SharePoint Lists - Data sources (AppPayrollCalendar2025, AppFMLARules, AppHandbookPolicies)

GitHub - Version control and documentation

ChatGPT & Gemini - Used for iterative logic building, debugging, and formula refinement

Perplexity AI - Assisted with contextual research and rule validation

### Connected SharePoint lists:

AppPayrollCalendar2025 - contains pay periods and holiday dates

AppFMLARules - defines FMLA-related rule flags

AppHandbookPolicies - stores internal policy references

## How It Works
### Users enter:

Due date

Optional work-from-home (WFH) start date

Whether PTO, unpaid days, or transition time will be used

### The app dynamically:

Builds a daily schedule using weekday logic

Inserts holidays that occur during the leave window

Extends leave types as needed to ensure full use of benefit days

Assigns each day a leave type, FMLA status, and associated pay period

The second screen displays the summary in a scrollable format - Example: Tuesday 08/26/2025 – Paid Child Care Leave | Pay Period: B091 (08/25/2025 - 09/07/2025) | FMLA: yes

Transition Plan dates will always display FMLA: no.

## Usage Notes

This version was built in June 2025. All calendar data references 2025. When testing, use 2025-based dates for accurate results. 

This app may show a delegation warning in Power Apps Studio due to certain Power Fx expressions. However, the datasets used are small and within the 2,000-row limit, so functionality is not affected in this implementation.

## Potential Future Enhancements

PDF or Excel export

Configurable leave types and durations

Support for additional languages or regional holiday rules

Integration with employee profile records 
